# HƯỚNG DẪN TẢI BỘ DỮ LIỆU BDD100K SEMANTIC SEGMENTATION (10K)

Tài liệu hướng dẫn tải và thiết lập bộ dữ liệu BDD100K 10K (7.000 ảnh Train, 1.000 ảnh Val, 19 nhãn chuẩn).

---

## 1. Link và cách tải (Chọn 1 trong 2 cách)

### Cách 1: Tải qua Kaggle (1 file zip trọn gói ~1.8 GB)
* Link tải: https://www.kaggle.com/datasets/solesensei/solesensei_bdd100k
* Bấm nút **Download** trên web để tải file `.zip` về máy.

### Cách 2: Tải bằng dòng lệnh từ máy chủ ETH Zurich
Chạy các lệnh sau trong terminal:
```bash
wget -c https://dl.cv.ethz.ch/bdd100k/data/10k_images_train.zip
wget -c https://dl.cv.ethz.ch/bdd100k/data/10k_images_val.zip
wget -c https://dl.cv.ethz.ch/bdd100k/data/bdd100k_sem_seg_labels_trainval.zip
```

---

## 2. Giải nén và đặt thư mục

Giải nén các file đã tải vào thư mục `data/` theo đúng cấu trúc sau:

```text
data/
└── bdd100k/
    ├── images/10k/
    │   ├── train/          # 7.000 ảnh .jpg
    │   └── val/            # 1.000 ảnh .jpg
    └── labels/sem_seg/
        └── masks/
            ├── train/      # 7.000 mask .png (pixel 0-18, 255)
            └── val/        # 1.000 mask .png
```

---

## 3. Kiểm tra sau khi giải nén

Chạy 2 lệnh sau để xác nhận số lượng file:
```bash
ls data/bdd100k/images/10k/train | wc -l    # Kết quả: 7000
ls data/bdd100k/images/10k/val | wc -l      # Kết quả: 1000
```
