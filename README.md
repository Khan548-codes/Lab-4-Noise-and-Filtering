# Lab-4-Noise-and-Filtering

Quick Summary of Noise Reduction Experiment
I started by messing up an original image using two common types of noise: Gaussian noise (the "fuzzy" kind) and salt & pepper noise (random black and white dots). This let me see how different kinds of noise degrade the picture (Section 1).

To measure the damage, I calculated the Mean Squared Error (MSE). Basically, a higher MSE means the noisy image is further away from the clean original (Section 2).

Then came the clean-up!

Linear Filters (Mean, Gaussian):
I first tried the simple average and Gaussian filters. They did reduce the noise, but the big downside was that they made the whole image look blurry, especially around edges (Section 3).

Non-linear Filter (Median): Next, I used the median filter. This one was a star, especially for the salt & pepper noise. Instead of blurring, it uses the middle value of the neighboring pixels, which completely removes those speckles while keeping the edges much sharper (Section 4).

By comparing the final MSE scores (Section 5), it was clear the median filter won the against salt & pepper noise.

What I Learned
The median filter is definitely the best tool for impulse noise like salt & pepper because it surgically removes the bright/dark dots without ruining the edges.

The average and Gaussian filters, being linear, just smooth everything out, which is why they blur the image so much. They can’t tell the difference between a noisy spot and a sharp edge.

If I were to do this again, I’d try an adaptive filter. That kind of filter is smart enough to check if a pixel is noise or part of an important edge, so it could filter heavily where needed and lightly everywhere else, giving us the best of both worlds.

![images](https://github.com/Khan548-codes/Lab-4-Noise-and-Filtering/blob/main/images/ss1.png)
![images](https://github.com/Khan548-codes/Lab-4-Noise-and-Filtering/blob/main/images/ss2.png)
![images](https://github.com/Khan548-codes/Lab-4-Noise-and-Filtering/blob/main/images/ss3.png)
