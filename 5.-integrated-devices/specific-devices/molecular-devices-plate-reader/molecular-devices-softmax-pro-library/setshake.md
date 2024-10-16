# SetShake

## Description

Shakes the microplate.\
When this command is set to true, starts shaking the microplate tray until the Shake(false) command is sent. By default, the shake will stop after 30 seconds in most instruments.

### Syntax

```
SetShake(i_blnShakeState)
```

### Arguments

\[in] i\_blnShakeStateASWGLOBAL::BOOL::TRUE to start the shaker\
ASWGLOBAL::BOOL::FALSE to stop the shaker\
\
