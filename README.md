# Example Data Wrangling Using Google Sheets

We will walk through an example of cleaning and visualizing the `1953-54_tvtrans_out.csv` dataset.

First, let's note some of the problems with data.

![img](https://i.imgur.com/Xw1Xm49.png)

![img](https://i.imgur.com/beFe55r.png)

Let's remove the comma and space with the `SUBSTITUTE` function.

![img](https://i.imgur.com/NYK99oH.png)

Thus, `4, 270` becomes `4270`.

![img](https://i.imgur.com/T65QpEE.png)

However, notice how `4270` is aligned to the left, rather than to the right? This indicates that `4270` is being stored as text, rather than as a value. We can convert `4270` to a value with the `VALUE` function by wrapping `VALUE` around `SUBSTITUTE`.

![img](https://i.imgur.com/HSE2RHD.png)

Now, 4270 is stored as a value.

![img](https://i.imgur.com/RwnFf9D.png)

Next, we will take this same logic and apply it to the entire dataset. Alternatively, you could manually go through the data, find the problem values and replace them. However, this leaves a lot of room for human error. Instead, we will remove `, ` from every cell in the dataset and convert every cell to a value (even if a cell already is stored as a value).

Here's what that looks like:

![img](https://i.imgur.com/GPlzHVh.png)

