# AvatarMe
Public repository for the CVPR paper AvatarMe.

### Overview

![Intro Image](img/avatarme_teaser.png "Teaser Image")

AvatarMe is the first method that is able to reconstruct photorealistic 3D faces from a single ‘in-the-wild” image with an increasing level of detail. To achieve this, we capture a large dataset of facial shape and reflectance and build on a state-of-the 3D texture and shape reconstruction method and successively refine its results in order to generate the high-resolution diffuse and specular components that are required for realistic rendering.

### Method

![Method Image](img/avatarme_method.png "Method Image")

A 3DMM is fitted to an ''in-the-wild'' input image 
and a completed UV texture is synthesized,
while optimizing for the identity match between the rendering and the input.
The texture is up-sampled 8 times,
to synthesize plausible high-frequency details.
We then use an image translation network to de-light the texture
and obtain the diffuse albedo with high-frequency details. 
Then, separate networks are used to infer the specular albedo,
diffuse normals and specular normals from the diffuse albedo and the 3DMM shape normals.
Moreover,
the networks are trained on 512x512 patches and inferences are ran on 1536x1536 patches with a sliding window.
Finally,
we can transfer the facial shape and the consistently inferred reflectance
to a head model.
Both face and head can be rendered realistically in any environment.

### Data
Information about the data will be anounced as soon as possible.
