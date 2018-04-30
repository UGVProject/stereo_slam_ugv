#### Operation Instruction for UGV stereo camera system

<i class="icon-book"></i> Note that SV2 is the main machine. So `roscore` should run on SV2.

<i class="icon-check"></i> Connect IMU wire, VGA wire to SV2.

<i class="icon-check"></i> Open both SV1 and SV2 Nuvo computers, so on the monitor we can see the desk of SV2.

<i class="icon-check"></i> Open VNC to remote connect SV1.  (If fails, try ssh -X ugv1@192.168.10.101)

<i class="icon-check"></i>  $UGV2: `roscore `

<i class="icon-check"></i> New terminal of SV2:
```
	$ugv2: sudo ntpdate -b ugv1.local
```
<i class="icon-check"></i> Open new terminal of SV2:
```
	$ugv1: roslaunch long.launch
```
<i class="icon-eye"></i> see if there is error displayed.
<i class="icon-camera-alt"></i> If no, that means camera has been set up successfully:

<i class="icon-check"></i> Open new terminal of SV1:
```
	$ugv1: roslaunch wide.launch
```


----------


Written by [<i class="icon-provider-github"></i> Handuo](https://zhanghanduo.github.io/)