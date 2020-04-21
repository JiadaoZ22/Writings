# Python ML

## Numpy

> - reshape
>
>   ```python
>   x = np.random.randint(min,max,shape)
>   x.reshape(-1, 1)
>   # produce a vertical vector
>   # x=[[1,2],[3,4,5]]
>   # output: [[1],[2],[3],[4],[5]]
>   ```
>
> - Selct by dimension
>
>   ```python
>   x = np.random.randint(min,max,shape)
>   idxes = np.random.randint(0, x.shape[0], y)
>   x[idxes]
>   ```
>
> - 
>   - 