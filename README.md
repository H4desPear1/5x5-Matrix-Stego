# 5x5-Matrix-Steg
This is a tool to encode or decode a 5x5 matrix cipher into/from an image.

The matrix is based off of this setup:
[a, b, c, d, e]
[f, g, h, i, j]
[k, l, m, n, o]
[p, q, r, s, t]
[u, v, w, x, y]

Each letter is then given two numbers based on their position within the matrix.
For example:
b = (1, 2) or r = (4, 3)
Where the first number is the row the letter is in and the second is the position within that row

For this encryption you use these coordinate points as directions for which pixels within the image to flip
Starting from the top left each letter is plotted out across the image

Each letter is then plotted based on the postion of the previous letter
For example:
If the first letter is h = (2, 3) and the second is i = (2, 4)
Then the first pixel that flips will be at (1, 2) (assuming that the top left is (0, 0)) and the second pixel that flips is (3, 6)

This will leave you with an image that has a descending set of flipped pixels
This set can then be decoded by reversing the process
