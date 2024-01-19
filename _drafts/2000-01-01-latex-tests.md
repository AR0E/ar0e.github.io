// Coding stuff

~~~ javascript
foreach joint in jointsTipToBase {
  // Point the effector towards the goal (See Above)

  // Constrain to rotate about the axis
  curHingeAxis = joint.rotation * joint.axis;
  hingeAxis = joint.parent.rotation * joint.axis;
  joint.rotateFromTo(curHingeAxis, hingeAxis);
}
~~~