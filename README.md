# JUDUL CONTENT
Penjelasan singkat dari content, disertai background / gambar struktur kerjanya.

contoh :
Split-and-Bridge: Adaptable Class Incremental Learning within a Single Neural Network in AAAI2021 by Jong-Yeong Kim and Dong-Wan Choi

<img src="https://user-images.githubusercontent.com/74110603/98468351-6d6a2180-221d-11eb-96ce-ad416da90100.png" width="85%" height="80%">

# Prerequisite code

## Environment
Hardware , Software, atau konfigurasi yang digunakan dimana program dibuat atau dijalankan.
 contoh : VS Code, IDE, PyTorch, JupyterLab, etc.

## Library
Kumpulan program pre-compiled, function atau data yang siap digunakan dalam program.
 contoh : numpy version 1.x, pandas version x.x , etc.

## Dataset
Kumpulan data yang digunakan dalam program, dapat diberikan detail seperti tipe data, struktur data, dan link tempat download datanya.
 contoh : dataset superstore, etc.

## User Guide
### Langkah penggunaan program

Disini dijelaskan dengan lengkap tata cara penggunaan program secara detail.
apabila diberikan contoh output dari program yang dijalankan, sertakan juga langkah-langkah atau command yang digunakan untuk mendapatkan hasil dari contoh output tersebut.

contoh:
Untuk mendapatkan hasil serupa dengan contoh program, dapat menjalankan potongan code berikut:
    
    python main.py --dataset CIFAR100 --trainer split -- base-classes 50 --step-size 50 --rho 1
    python main.py --dataset CIFAR100 --trainer split -- base-classes 20 --step-size 20 --rho 1.35
    python main.py --dataset CIFAR100 --trainer split -- base-classes 10 --step-size 10 --rho 1.15
    python main.py --dataset CIFAR100 --trainer split -- base-classes 5 --step-size 5 --rho 1

Untuk output yang mengeluarkan beberapa hasil, dapat di compile menjadi sebuah table agar memudahkan untuk dibaca.

contoh:

|Number of tasks|2|5|10|20|
|-----------------|---|---|---|---|
|STD with iCaRL|68.02|63.0|58.05|60.36|
|STD with Bic|**70.13**|68.22|61.10|48.68|
|STD with WA|69.72|68.73|63.98|54.93|
|DD with WA|69.34|68.53|63.77|57.03|
|S&B with WA (ours)|69.77|**69.76**|**67.56**|**61.52**|

## Konfigurasi Optional
Sertakan disini konfigurasi opsional yang dapat disesuaikan oleh pengguna lainnya untuk menunjang hasil dari output.

contoh :
*Optional*: 
* `--batch-size`: input batch size for training. *type*: `int`, *Default*: `256`
* `--workers`: Number of workers in Dataloaders. *type*: `int`, *Default*: `0`
* `--nepochs`: Number of epochs for each increment. *type*: `int`, *Default*: `200`
* `--lr`: learning rate. *type*: `float`, *Default*: `0.1`
* `--schedule`: Decrease learning rate at these epochs. *type*: `int`, *Default*: `[60,120,160]`
* `--gammas`: LR is multiplied by gamma on schedule, number of gammas should be equal to schedule. *type*: `float`, *Default*: `[0.1, 0.1,0.1]`
* `--momentum`: SGD momentum. *type*: `float`, *Default*: `0.9`
* `--decay`: Weight decay (L2 penalty). *type*: `float`, *Default*: `0.0005`
* `--base-classes`: Number of base classe. *type*: `int`, *Default*: `20`
* `--step-size`: How many classes to add in each increment. *type*: `int`, *Default*: `20`
* `--memory-budget`: How many images can we store at max. *type*: `int`, *Default*: `2000`
* `--rho`: adaptive split hyperparameter. *type*: `float`, *Default*: `1`
* `--seed`: Seeds values to be used; seed introduces randomness by changing order of classes. *type*: `int`, *Default*: `0`



## Acknowledgements

This implementation has been tested with Pytorch 1.2.0 on Windows 10.
