# sage60 用の改変

[sage60](https://github.com/Diwamoto/sage60) で使うトラックボールケースとセンサー基板の置き場所。sage60 本体は MIT で、GPL の部分をここに分けている。

| パス | 中身 | 変更 |
| --- | --- | --- |
| `pcb/pmw3610_breakout_for_roBa/` | PMW3610 センサー基板 | なし（roBa のまま） |
| `case/trackballcase.stl` | トラックボールケースの元データ（git LFS） | なし（roBa のまま） |
| `sage60/trackballcase_low.3mf` | 改変したケース（プリント用） | 下記 |
| `sage60/trackballcase_low.stl` | 上と同じ形を z+2 した STL。sage60 のケース生成スクリプトが読む | 下記 |

## 変更点（Diwamoto、2026-10）

- 2026-10-20: 低くし、+x 側を 2.7mm 短くした
- 2026-10-28: J1 の丸ピンソケットを通す切り欠きを追加し、基板の舌の上の下面を上げた
- 2026-10-29: ネジの耳を φ6×3 磁石の保持部にした

10-28 と 10-29 の加工は sage60 の [`case/trackball/tb_socket_cut.py`](https://github.com/Diwamoto/sage60/blob/master/case/trackball/tb_socket_cut.py) で行った。

## ライセンス

- このリポジトリ全体: GPL-3.0（`LICENSE`、[kumamuk-git/roBa](https://github.com/kumamuk-git/roBa) から継承）
- ケース: [Keyball Trackball Case](https://www.thingiverse.com/thing:6215791) © kepeo（[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)）を roBa が改変し、それをさらに改変したもの
