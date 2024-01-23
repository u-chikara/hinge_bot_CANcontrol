# hinge_bot_CANcontrol

PS4コントローラーの入力データーをそのままCANで送る。

レート:60fps

CANID:0x7ff

送るデーターは以下のとおりである。

| bit | 0 to 7  |
| --  | ---- |
| 0byte  | アナログスティックLX  |
| 1byte  | アナログスティックLY  |
| 2byte  | アナログスティックRX  |
| 3byte  | アナログスティックRY  |
| 4byte  | アナログレバーL  |
| 5byte  | アナログレバーR  |

| bit | 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  |
| --  | -- | -- | -- | -- | -- | -- | -- | -- |
| 6byte  | UP  | RIGHT  | DOWN  | LEFT  | TRIANGLE  | CIRCLE  | CROSS  | RECTANGLE  |
| 7byte  | L1  | R1  | LSW  | RSW  | SHARE  | OPTIONS  | TOUCHPAD  | NULL  |

アナログスティックは-128から127

デッドゾーンは設けなくてよい。

アナログレバーは0から255

ボタンは押されると対応のビットが1に、押されていない場合は0になる。
