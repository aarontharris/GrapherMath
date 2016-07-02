# GrapherMath
Mac Grapher Math Models for various projects

Open .gcx files with Grapher on your Mac.

#FYI
I'm not a mathematician, I'm just an engineer with mediocre math skills at best. Most of these models are not intended to be true to reality but rather an adaptation for gaming so please judge accordingly.

Apologies to Windows users, I don't know of an equivalent tool for Windows and I really love Mac Grapher :)

My models are typically broken out for the sake of easy translation to code.  I typically use these for game development which ends up as C if I'm doing SDL/OpenGL or C# if I'm using Unity.  The theme you will hopefully find is math functions with abstracted parameters for the sake of readability and simple functions as you might find them in code.  I try to scope my functions, function variables and group variables with a prefix for namespacing to reduce collisions and confusion -- Grapher isn't very good at that.

Prefixes:
* m = member, I use this for group scoped variables, likely to be member variables when converted to code.
* p = parameter, I use this for function scoped parameters
* f = function

# Gravity.gcx
Gravity for games.

```
// Obtain the influence of gravity between the source and an objects distance from the source.
// Note that the smaller your maxReach is, the less accurate gravity will be compared to reality since true gravity falloff is an extreme distance.
//
// params:
// magnitude is the strength of gravity at the surface
// surfRadius is the distance from the center to the surface
// maxReach is the distance from the center that the influence reaches zero.
// dist is the objects distance from the gravity source.
//
// return:
// the magnitude of influence on the object give its distence from the center of the gravity source.
fGravityFalloff(pMagnitude, pSurfRadius, pMaxReach, pDist)
```

