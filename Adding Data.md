Instead of getting more data of every type in the dataset, focus on adding more data for the types where error analysis has indicated it might help.

# Data Augmentation

For image data, we can take the training examples and apply transformations like cropping, rotating, or mirroring the images. Additionally, we can add distortions to the images to create new variants, which enrich the dataset.

![[Pasted image 20241010130634.png]]

For audio data, we can augment them by introducing background noise or disturbances, simulating real-world conditions.

![[Pasted image 20241010130807.png]]

When working with images of letters, we can use different fonts, colors, contrasts, and other visual variations from a computer to create augmented examples.

It's important to augment the data in ways that improve the algorithm's learning rather than confusing it with irrelevant variations. Carefully chosen augmentations help the model generalize better to unseen data.
