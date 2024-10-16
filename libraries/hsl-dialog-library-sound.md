# HSL Dialog Library (sound)

The HSL Dialog Library provides the following function:

&#x20;

DlgPlaySound

&#x20;

Include: HSLDlgLib.hsl

&#x20;

| Function                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| -------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p> </p><p>DlgPlaySound(</p><p>variable&#x26; sound)</p> | <p> </p><p>Plays a sound specified by the given file name, or system event (a system event may be associated with a sound in the registry or in the WIN.INI file).</p><p> </p><p>Parameter:</p><p>sound</p><p>A string that specifies the sound to play. If this parameter is empty, any currently playing waveform sound is stopped.</p><p>If sound specifies a file name it can be relative or absolute. In this case, the file specified will be searched in the following directories in the following sequence:</p><p>1) in the current directory.</p><p>2) in the directory that is listed under the registry key Methods.</p><p>3) in the directory that is listed under the registry key Library.</p><p>4) in the directories that are listed in the PATH environment variable.</p><p> </p><p>Return:</p><p>If the function succeeds, the return value is nonzero.</p><p>If the function fails, the return value is zero.</p><p> </p> |
