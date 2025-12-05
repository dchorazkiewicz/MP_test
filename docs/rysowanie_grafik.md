# Wykres funkcji kwadratowej $f(x) = x^2$

```python mkdocs-matplotlib
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-5, 5, 100)
y = x**2

plt.figure(figsize=(6, 4))
plt.plot(x, y, label='$y = x^2
)
plt.title('Wykres funkcji kwadratowej')
plt.xlabel('Oś X')
plt.ylabel('Oś Y')
plt.grid(True)
plt.legend()
plt.show()
```
