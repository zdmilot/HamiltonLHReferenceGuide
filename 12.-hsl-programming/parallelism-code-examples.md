# Parallelism Code Examples

#### Remarks

* The units of parallel execution are functions.
* Any data has to be passed into a function that a new thread is to execute by global variables.
* Threads are synchronized by events, or timers, or by calling the Join function.
* Events are the only objects that allow one thread mutually exclusive access to a resource (data).

&#x20;

#### Example

Using functions as entry points to new threads:

<pre class="language-clike"><code class="lang-clike">device swap("SystemDeckLayout.lay", "ML_SWAP", hslTrue);

device star("SystemDeckLayout.lay", "ML_STAR", hslTrue);

 

function SWAPInit()

{

 swap.Initialize("be5b5ed0_1bf7_11d4_b878002035848439");
 
 return;

}

 

function STARInit()

{

 star.Initialize("ce5b5ed0_1bf7_11d4_b878002035848439");
 
 return;

}

 

method Main()

{

<strong> variable rc(0);
</strong> 
 variable timeout(2*60);
 
 variable handle;
 
 variable handles[ ];
 
 onerror goto ErrorHandler;
 
  
 
 // initialize STAR and SWAP in parallel using separate threads
 
  
 
 handle = Fork("SWAPInit");
 
 if (0 == handle)
 
 err.Raise(0, "Failed to fork SWAPInit");
 
 handles.AddAsLast(handle);
 
 handle = Fork("STARInit");
 
 if (0 == handle)
 
 err.Raise(0, "Failed to fork STARInit");
 
 handles.AddAsLast(handle);
 
  
 
 // do anything else in the main thread, before waiting until STAR and SWAP have been initialized
 
  
 
 rc = Join(handles, timeout);
 
 if (0 == rc)
 
 err.Raise(1, "Failed to join handles");
 
 return;
 
  
 
 ErrorHandler :

{

if (hslAbort == MessageBox( err.GetDescription(), "Error - Main", hslError|hslAbortRetryIgnore))

abort;

resume next;

}

}
</code></pre>

