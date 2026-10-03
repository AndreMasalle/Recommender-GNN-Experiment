# Recommender GNN Experiment

<p align="center">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/PyTorchGeometric-3C2179?logo=pyg&logoColor=white" alt="PyTorch Geometric">
  <img src="https://img.shields.io/badge/NetworkX-2C7FB8" alt="NetworkX">
</p>

## Deskripsi

Repositori ini berisi catatan belajar dan eksperimen pribadi dalam mempelajari
**Graph Neural Network (GNN) untuk sistem rekomendasi (recommender systems)**.

Fokus pembelajaran mencakup:

- Konsep dasar **message passing** dan **graph convolution** (GCN).
- Penerapan GNN untuk tugas-tugas recommender
- Pembelajaran representasi node (node embedding) pada graf interaksi
  user-item.
- Eksperimen arsitektur: jumlah layer, hidden channel, dropout, dan
  fungsi aktivasi.

Repositori ini murni untuk **pembelajaran**, bukan library produksi. Kode
ditulis untuk memahami konsep, sehingga mungkin belum dioptimasi.

---

## Sumber

Materi dan implementasi dalam repositori ini dipelajari dari:

| Sumber | Jenis | Topik |
|:---|:---|:---|
| *Advancing Recommender Systems with Graph Convolutional Networks* | Buku | Teori GCN untuk recommender systems |
| DataCamp - Graph Neural Networks | Course | Praktik GNN dengan PyTorch Geometric |
| [PyTorch Geometric Documentation](https://pytorch-geometric.readthedocs.io/) | Dokumentasi | Referensi API `GCNConv`, `GraphSAGE`, `GAT`, dll. |
| [KONECT](http://konect.cc/) | Dataset | Dataset graf untuk eksperimen |

## Dataset

- **Planetoid - Cora** - dataset sitasi standar untuk eksperimen GNN.

  ```python
  from torch_geometric.datasets import Planetoid
  from torch_geometric.transforms import NormalizeFeatures

  dataset = Planetoid(
      root='data/Planetoid',
      name='Cora',
      transform=NormalizeFeatures(),
  )
  ```

  Informasi dataset:

  - Number of graphs: 1
  - Number of features: 1433
  - Number of classes: 7
  - Jumlah node: 2.708
  - Jumlah edge: 10.556

---

*README ini akan diperbarui seiring bertambahnya materi dan eksperimen.*