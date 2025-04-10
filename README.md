simple-knn
---

Description: It compute the **average distance to the nearest neighbors** for a set of 3D points.

Install:
```bash
pip install git+https://github.com/coder-bryan-123/simple-knn

# or 
git clone https://github.com/coder-bryan-123/simple-knn && cd simple-knn
pip install .
```

Usage:
```python
from simple_knn._C import distCUDA2

# shape: [N, 3]
demopc = torch.from_numpy(np.load("/path")).float().cuda().contiguous() 

# shape: [N]
mean_distances = distCUDA2(demopc)
```

Tests:
```
# no validation currently
python tests/knn_test.py
```