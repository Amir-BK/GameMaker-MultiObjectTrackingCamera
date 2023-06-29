# GameMaker-MultiObjectTrackingCamera
A simple camera system that can track multiple objects while zooming in and out to keep them all in view 

Also available in the gamemaker marketplace - https://marketplace.yoyogames.com/assets/10066/multi-object-tracking-camera

#Usage
Either install as plugin or just import the camera object into your project and then just place the 'MultiTrackCamera' object in the room, and then add objects to be tracked using the Track_Objects(object_to_track) function (which can be called from the MultiTrackCamera object itself or from any other object using dot notation "MultiTrackCamera.Track_Objects(object)"). As the function uses a with() statement it can accept object index or instance id so you can choose to either track a single instance or any instance of a certain object. For added convenience it is also possible to pass an array of objects\instances to the same function like this "MultiTrackCamera.Track_Objects([object1, object2, object3...])".

To stop tracking an object\instance use the "Stop_Tracking_Objects(object_or_instance_or_array)" function. Note that if some object is tracked both as an instance and as part of an object_index removing its instance from the tracked object array will not actually stop the tracking. A Stop_Tracking_All() method is also provided.

