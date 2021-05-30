## 学籍番号
21M30985

## 氏名
伊藤巧

# 実行方法
qrsh -g tga-hpc-lecture -l f_node=1 -l h_rt=1:00:00

module load intel-mpi gcc

mpicxx example.cpp -fopenmp -fopt-info-vec-optimized -march=native -O3

mpirun -np 1 ./a.out

# ファイルについて
original.cppはもともと提供されていたコード、example.cppは提出コードになります。

original.cppの実行結果はoutput_original.txtへ、
example.cppの実行結果はoutput_example.txtへ書かれています。

実行速度の関係でoriginal.cppはN=256,512,1024、
example.cppはN=256,512,1024,2048,4096,8192において実行しています。
