# CVE-2020-10135-BIAS
CVE 2020-10135 a.k.a BIAS (Bluetooth Impersonation Attack)

Seems like after a while and jumping through some hoops was able to perform BIAS (Bluetooth Impersonation Attack) CVE 2020-10135. Impersonated Samsung S3 Neo+ connection to Linux host. Cool stuff. THANK YOU for Internalblue and BIAS PoCs.

From my perspective found out that pretty much all you need to perform the attack is the BT address of inpersonated device that was previously paired and connected with the other end. Rest you can obtain for PoC to work.

![CVE-2020-10135](bias.jpeg)

PoC/original Author(s):
https://github.com/francozappa/bias

LOG

```

No.     Time           Source                Destination           Protocol Length Info
      1 0.000000       2f:d0:a5:b4           controller            LMP      64     LMP_version_req

Frame 1: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      2 0.016282       controller            2f:d0:a5:b4           LMP      64     LMP_version_res

Frame 2: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      3 0.016293       2f:d0:a5:b4           controller            LMP      64     LMP_features_req

Frame 3: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      4 0.016295       controller            2f:d0:a5:b4           LMP      64     LMP_features_res

Frame 4: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      5 0.032274       2f:d0:a5:b4           controller            LMP      64     LMP_features_req_ext

Frame 5: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      6 0.032285       controller            2f:d0:a5:b4           LMP      64     LMP_features_res_ext

Frame 6: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      7 0.032287       2f:d0:a5:b4           controller            LMP      64     LMP_power_control_req

Frame 7: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      8 0.048306       2f:d0:a5:b4           controller            LMP      64     LMP_host_connection_req

Frame 8: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
      9 0.048313       controller            host                  HCI_EVT  13     Rcvd Connect Request

Frame 9: 13 bytes on wire (104 bits), 13 bytes captured (104 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Connect Request

No.     Time           Source                Destination           Protocol Length Info
     10 0.048319       controller            2f:d0:a5:b4           LMP      64     LMP_power_control_res

Frame 10: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     11 0.048415       host                  controller            HCI_CMD  11     Sent Accept Connection Request

Frame 11: 11 bytes on wire (88 bits), 11 bytes captured (88 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - Accept Connection Request

No.     Time           Source                Destination           Protocol Length Info
     12 0.063970       controller            host                  HCI_EVT  7      Rcvd Command Status (Accept Connection Request)

Frame 12: 7 bytes on wire (56 bits), 7 bytes captured (56 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Status

No.     Time           Source                Destination           Protocol Length Info
     13 0.080314       controller            2f:d0:a5:b4           LMP      64     LMP_slot_offset

Frame 13: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     14 0.080320       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 14: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     15 0.096284       controller            2f:d0:a5:b4           LMP      64     LMP_switch_req

Frame 15: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     16 0.096294       2f:d0:a5:b4           controller            LMP      64     LMP_power_control_req

Frame 16: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     17 0.256055       controller            2f:d0:a5:b4           LMP      64     LMP_power_control_res

Frame 17: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     18 0.256066       controller            2f:d0:a5:b4           LMP      64     LMP_slot_offset

Frame 18: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     19 0.256067       controller            2f:d0:a5:b4           LMP      64     LMP_switch_req

Frame 19: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     20 0.272129       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 20: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     21 0.400080       controller            host                  HCI_EVT  11     Rcvd Role Change

Frame 21: 11 bytes on wire (88 bits), 11 bytes captured (88 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Role Change

No.     Time           Source                Destination           Protocol Length Info
     22 0.416072       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 22: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     23 0.416083       2f:d0:a5:b4           controller            LMP      64     LMP_setup_complete

Frame 23: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     24 0.416085       controller            2f:d0:a5:b4           LMP      64     LMP_set_AFH

Frame 24: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     25 0.431918       controller            host                  HCI_EVT  14     Rcvd Connect Complete

Frame 25: 14 bytes on wire (112 bits), 14 bytes captured (112 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Connect Complete

No.     Time           Source                Destination           Protocol Length Info
     26 0.431945       controller            2f:d0:a5:b4           LMP      64     LMP_channel_classification_req

Frame 26: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     27 0.431946       controller            2f:d0:a5:b4           LMP      64     LMP_setup_complete

Frame 27: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     28 0.432247       host                  controller            HCI_CMD  6      Sent Read Remote Supported Features

Frame 28: 6 bytes on wire (48 bits), 6 bytes captured (48 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - Read Remote Supported Features

No.     Time           Source                Destination           Protocol Length Info
     29 0.447753       controller            2f:d0:a5:b4           LMP      64     LMP_max_slot

Frame 29: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     30 0.447765       2f:d0:a5:b4           controller            LMP      64     LMP_channel_classification

Frame 30: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     31 0.447767       controller            2f:d0:a5:b4           LMP      64     LMP_max_slot_req

Frame 31: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     32 0.463744       controller            2f:d0:a5:b4           LMP      64     LMP_auto_rate

Frame 32: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     33 0.463756       2f:d0:a5:b4           controller            LMP      64     LMP_timing_accuracy_req

Frame 33: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     34 0.463759       controller            2f:d0:a5:b4           LMP      64     LMP_timing_accuracy_res

Frame 34: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     35 0.479943       2f:d0:a5:b4           controller            LMP      64     LMP_auto_rate

Frame 35: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     36 0.479954       2f:d0:a5:b4           controller            LMP      64     LMP_max_slot_req

Frame 36: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     37 0.479956       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 37: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     38 0.479958       controller            host                  HCI_EVT  6      Rcvd Max Slots Change

Frame 38: 6 bytes on wire (48 bits), 6 bytes captured (48 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Max Slots Change

No.     Time           Source                Destination           Protocol Length Info
     39 0.496056       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 39: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     40 0.496072       controller            2f:d0:a5:b4           LMP      64     LMP_timing_accuracy_req

Frame 40: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     41 0.496074       2f:d0:a5:b4           controller            LMP      64     LMP_power_control_req

Frame 41: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     42 0.511967       2f:d0:a5:b4           controller            LMP      64     LMP_preferred_rate

Frame 42: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     43 0.512048       controller            2f:d0:a5:b4           LMP      64     LMP_power_control_res

Frame 43: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     44 0.512090       2f:d0:a5:b4           controller            LMP      64     LMP_timing_accuracy_res

Frame 44: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     45 0.528026       2f:d0:a5:b4           controller            LMP      64     LMP_features_req

Frame 45: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     46 0.528039       controller            2f:d0:a5:b4           LMP      64     LMP_features_res

Frame 46: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     47 0.543872       2f:d0:a5:b4           controller            LMP      64     LMP_features_req_ext

Frame 47: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     48 0.543926       controller            2f:d0:a5:b4           LMP      64     LMP_features_res_ext

Frame 48: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     49 0.543928       2f:d0:a5:b4           controller            LMP      64     LMP_features_req_ext

Frame 49: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     50 0.543930       controller            host                  HCI_EVT  7      Rcvd Command Status (Read Remote Supported Features)

Frame 50: 7 bytes on wire (56 bits), 7 bytes captured (56 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Status

No.     Time           Source                Destination           Protocol Length Info
     51 0.543932       controller            host                  HCI_EVT  14     Rcvd Read Remote Supported Features

Frame 51: 14 bytes on wire (112 bits), 14 bytes captured (112 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Read Remote Supported Features

No.     Time           Source                Destination           Protocol Length Info
     52 0.544086       host                  controller            HCI_CMD  7      Sent Read Remote Extended Features

Frame 52: 7 bytes on wire (56 bits), 7 bytes captured (56 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - Read Remote Extended Features

No.     Time           Source                Destination           Protocol Length Info
     53 0.559996       controller            2f:d0:a5:b4           LMP      64     LMP_features_res_ext

Frame 53: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     54 0.560009       2f:d0:a5:b4           controller            LMP      64     LMP_name_req

Frame 54: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     55 0.560011       controller            2f:d0:a5:b4           LMP      64     LMP_name_res

Frame 55: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     56 0.560013       controller            host                  HCI_EVT  7      Rcvd Command Status (Read Remote Extended Features)

Frame 56: 7 bytes on wire (56 bits), 7 bytes captured (56 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Status

No.     Time           Source                Destination           Protocol Length Info
     57 0.560014       controller            host                  HCI_EVT  16     Rcvd Read Remote Extended Features Complete

Frame 57: 16 bytes on wire (128 bits), 16 bytes captured (128 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Read Remote Extended Features Complete

No.     Time           Source                Destination           Protocol Length Info
     58 0.560122       host                  controller            HCI_CMD  14     Sent Remote Name Request

Frame 58: 14 bytes on wire (112 bits), 14 bytes captured (112 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - Remote Name Request

No.     Time           Source                Destination           Protocol Length Info
     59 0.560134       localhost ()          LiteonTe_d0:a5:b4 ()  L2CAP    15     Sent Information Request (Extended Features Mask)

Frame 59: 15 bytes on wire (120 bits), 15 bytes captured (120 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
     60 0.576035       controller            2f:d0:a5:b4           LMP      64     LMP_set_AFH

Frame 60: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     61 0.576040       controller            host                  HCI_EVT  7      Rcvd Command Status (Remote Name Request)

Frame 61: 7 bytes on wire (56 bits), 7 bytes captured (56 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Status

No.     Time           Source                Destination           Protocol Length Info
     62 0.576042       controller            2f:d0:a5:b4           LMP      64     LMP_name_req

Frame 62: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     63 0.608037       controller            host                  HCI_EVT  258    Rcvd Remote Name Request Complete

Frame 63: 258 bytes on wire (2064 bits), 258 bytes captured (2064 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Remote Name Request Complete

No.     Time           Source                Destination           Protocol Length Info
     64 0.608048       2f:d0:a5:b4           controller            LMP      64     LMP_name_res

Frame 64: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     65 0.608050       controller            host                  HCI_EVT  9      Rcvd Link Key Request

Frame 65: 9 bytes on wire (72 bits), 9 bytes captured (72 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Link Key Request

No.     Time           Source                Destination           Protocol Length Info
     66 0.608052       2f:d0:a5:b4           controller            LMP      64     LMP_au_rand

Frame 66: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     67 0.608139       host                  controller            HCI_CMD  10     Sent Link Key Request Negative Reply

Frame 67: 10 bytes on wire (80 bits), 10 bytes captured (80 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - Link Key Request Negative Reply

No.     Time           Source                Destination           Protocol Length Info
     68 0.623659       controller            host                  HCI_EVT  13     Rcvd Command Complete (Link Key Request Negative Reply)

Frame 68: 13 bytes on wire (104 bits), 13 bytes captured (104 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Complete

No.     Time           Source                Destination           Protocol Length Info
     69 0.623670       controller            2f:d0:a5:b4           LMP      64     LMP_not_accepted

Frame 69: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     70 0.623672       controller            host                  HCI_EVT  12     Rcvd IO Capability Response

Frame 70: 12 bytes on wire (96 bits), 12 bytes captured (96 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - IO Capability Response

No.     Time           Source                Destination           Protocol Length Info
     71 0.623673       controller            host                  HCI_EVT  9      Rcvd IO Capability Request

Frame 71: 9 bytes on wire (72 bits), 9 bytes captured (72 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - IO Capability Request

No.     Time           Source                Destination           Protocol Length Info
     72 0.623720       host                  controller            HCI_CMD  13     Sent IO Capability Request Reply

Frame 72: 13 bytes on wire (104 bits), 13 bytes captured (104 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - IO Capability Request Reply

No.     Time           Source                Destination           Protocol Length Info
     73 0.639626       2f:d0:a5:b4           controller            LMP      64     LMP_IO_Capability_req

Frame 73: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     74 0.639631       controller            host                  HCI_EVT  13     Rcvd Command Complete (IO Capability Request Reply)

Frame 74: 13 bytes on wire (104 bits), 13 bytes captured (104 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Complete

No.     Time           Source                Destination           Protocol Length Info
     75 0.639638       controller            2f:d0:a5:b4           LMP      64     LMP_IO_Capability_res

Frame 75: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     76 0.767608       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 76: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
     77 0.863855       2f:d0:a5:b4           controller            LMP      64     LMP_encapsulated_header

Frame 77: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     78 0.863860       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 78: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     79 0.879828       2f:d0:a5:b4           controller            LMP      64     LMP_encapsulated_payload

Frame 79: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     80 0.879840       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 80: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     81 0.879843       2f:d0:a5:b4           controller            LMP      64     LMP_encapsulated_payload

Frame 81: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     82 0.895821       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 82: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     83 0.911566       2f:d0:a5:b4           controller            LMP      64     LMP_encapsulated_payload

Frame 83: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     84 0.911581       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 84: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     85 0.911583       controller            2f:d0:a5:b4           LMP      64     LMP_encapsulated_header

Frame 85: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     86 0.927824       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 86: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     87 0.927838       controller            2f:d0:a5:b4           LMP      64     LMP_encapsulated_payload

Frame 87: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     88 0.927840       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 88: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     89 0.943818       controller            2f:d0:a5:b4           LMP      64     LMP_encapsulated_payload

Frame 89: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     90 0.943830       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 90: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     91 0.943832       controller            2f:d0:a5:b4           LMP      64     LMP_encapsulated_payload

Frame 91: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     92 0.959743       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 92: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     93 0.959755       controller            2f:d0:a5:b4           LMP      64     LMP_Simple_Pairing_Confirm

Frame 93: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     94 1.151601       2f:d0:a5:b4           controller            LMP      64     LMP_Simple_Pairing_Number

Frame 94: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     95 1.151614       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 95: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     96 1.151617       controller            2f:d0:a5:b4           LMP      64     LMP_Simple_Pairing_Number

Frame 96: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
     97 1.151619       controller            host                  HCI_EVT  13     Rcvd User Confirmation Request

Frame 97: 13 bytes on wire (104 bits), 13 bytes captured (104 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - User Confirmation Request

No.     Time           Source                Destination           Protocol Length Info
     98 1.151705       host                  controller            HCI_CMD  10     Sent User Confirmation Request Reply

Frame 98: 10 bytes on wire (80 bits), 10 bytes captured (80 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - User Confirmation Request Reply

No.     Time           Source                Destination           Protocol Length Info
     99 1.167607       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 99: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    100 1.167620       2f:d0:a5:b4           controller            LMP      64     LMP_DHkey_Check

Frame 100: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    101 1.167623       controller            host                  HCI_EVT  13     Rcvd Command Complete (User Confirmation Request Reply)

Frame 101: 13 bytes on wire (104 bits), 13 bytes captured (104 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Complete

No.     Time           Source                Destination           Protocol Length Info
    102 1.183608       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 102: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    103 1.183623       controller            2f:d0:a5:b4           LMP      64     LMP_DHkey_Check

Frame 103: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    104 1.183626       controller            host                  HCI_EVT  10     Rcvd Simple Pairing Complete

Frame 104: 10 bytes on wire (80 bits), 10 bytes captured (80 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Simple Pairing Complete

No.     Time           Source                Destination           Protocol Length Info
    105 1.183628       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 105: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    106 1.199610       2f:d0:a5:b4           controller            LMP      64     LMP_au_rand

Frame 106: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    107 1.199625       controller            2f:d0:a5:b4           LMP      64     LMP_sres

Frame 107: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    108 1.199628       controller            2f:d0:a5:b4           LMP      64     LMP_au_rand

Frame 108: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    109 1.199630       controller            host                  HCI_EVT  26     Rcvd Link Key Notification

Frame 109: 26 bytes on wire (208 bits), 26 bytes captured (208 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Link Key Notification

No.     Time           Source                Destination           Protocol Length Info
    110 1.215331       2f:d0:a5:b4           controller            LMP      64     LMP_sres

Frame 110: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    111 1.215348       2f:d0:a5:b4           controller            LMP      64     LMP_encryption_mode_req

Frame 111: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    112 1.231632       controller            2f:d0:a5:b4           LMP      64     LMP_accepted

Frame 112: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    113 1.231644       controller            2f:d0:a5:b4           LMP      64     LMP_encryption_key_size_req

Frame 113: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    114 1.231646       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 114: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    115 1.247412       controller            2f:d0:a5:b4           LMP      64     LMP_start_encryption_req

Frame 115: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    116 1.247423       controller            host                  HCI_EVT  7      Rcvd Encryption Change

Frame 116: 7 bytes on wire (56 bits), 7 bytes captured (56 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Encryption Change

No.     Time           Source                Destination           Protocol Length Info
    117 1.247432       2f:d0:a5:b4           controller            LMP      64     LMP_accepted

Frame 117: 64 bytes on wire (512 bits), 64 bytes captured (512 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth H4 Serial Broadcom Vendor Specific

No.     Time           Source                Destination           Protocol Length Info
    118 1.247437       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    15     Rcvd Information Request (Extended Features Mask)

Frame 118: 15 bytes on wire (120 bits), 15 bytes captured (120 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    119 1.247438       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    21     Rcvd Information Response (Extended Features Mask, Success)

Frame 119: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    120 1.247567       host                  controller            HCI_CMD  6      Sent Read Encryption Key Size

Frame 120: 6 bytes on wire (48 bits), 6 bytes captured (48 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Command - Read Encryption Key Size

No.     Time           Source                Destination           Protocol Length Info
    121 1.247585       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Information Response (Extended Features Mask, Success)

Frame 121: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    122 1.247590       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    15     Sent Information Request (Fixed Channels Supported)

Frame 122: 15 bytes on wire (120 bits), 15 bytes captured (120 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    123 1.263339       controller            host                  HCI_EVT  10     Rcvd Command Complete (Read Encryption Key Size)

Frame 123: 10 bytes on wire (80 bits), 10 bytes captured (80 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Command Complete

No.     Time           Source                Destination           Protocol Length Info
    124 1.263345       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 124: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    125 1.263346       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    15     Rcvd Information Request (Fixed Channels Supported)

Frame 125: 15 bytes on wire (120 bits), 15 bytes captured (120 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    126 1.263347       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    25     Rcvd Information Response (Fixed Channels Supported, Success)

Frame 126: 25 bytes on wire (200 bits), 25 bytes captured (200 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    127 1.263390       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    25     Sent Information Response (Fixed Channels Supported, Success)

Frame 127: 25 bytes on wire (200 bits), 25 bytes captured (200 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    128 1.279288       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    17     Rcvd Connection Request (AVDTP, SCID: 0x0040)

Frame 128: 17 bytes on wire (136 bits), 17 bytes captured (136 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    129 1.279351       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Connection Response - Pending (SCID: 0x0040)

Frame 129: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    130 1.279617       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Connection Response - Success (SCID: 0x0040, DCID: 0x0040)

Frame 130: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    131 1.279631       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    28     Sent Configure Request (DCID: 0x0040)

Frame 131: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    132 1.295304       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 132: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    133 1.295312       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    28     Rcvd Configure Request (DCID: 0x0040)

Frame 133: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    134 1.295388       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    23     Sent Configure Response - Success (SCID: 0x0040)

Frame 134: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    135 1.311596       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 135: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    136 1.311603       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    23     Rcvd Configure Response - Success (SCID: 0x0040)

Frame 136: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    137 1.311604       LiteonTe_d0:a5:b4 (laptop) localhost ()          AVDTP    11     Rcvd Command - Discover

Frame 137: 11 bytes on wire (88 bits), 11 bytes captured (88 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    138 1.315729       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVDTP    15     Sent ResponseAccept - Discover - items: 2

Frame 138: 15 bytes on wire (120 bits), 15 bytes captured (120 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    139 1.327269       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 139: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    140 1.327276       LiteonTe_d0:a5:b4 (laptop) localhost ()          AVDTP    12     Rcvd Command - GetCapabilities - ACP SEID [1 - Audio Source]

Frame 140: 12 bytes on wire (96 bits), 12 bytes captured (96 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    141 1.327441       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVDTP    21     Sent ResponseAccept - GetCapabilities - Audio SBC (16000 32000 44100 48000 | Mono DualChannel Stereo JointStereo | block: 4 8 12 16 | subbands: 4 8 | allocation: SNR Loudness | bitpool: 2..64)

Frame 141: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    142 1.343594       LiteonTe_d0:a5:b4 (laptop) localhost ()          AVDTP    12     Rcvd Command - GetCapabilities - ACP SEID [2 - Audio Sink]

Frame 142: 12 bytes on wire (96 bits), 12 bytes captured (96 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    143 1.343796       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVDTP    21     Sent ResponseAccept - GetCapabilities - Audio SBC (16000 32000 44100 48000 | Mono DualChannel Stereo JointStereo | block: 4 8 12 16 | subbands: 4 8 | allocation: SNR Loudness | bitpool: 2..64)

Frame 143: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    144 1.359315       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 144: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    145 1.359322       LiteonTe_d0:a5:b4 (laptop) localhost ()          AVDTP    23     Rcvd Command - SetConfiguration - ACP SEID [1 - Audio Source] - INT SEID [4 - Audio Source] - Audio SBC (44100 | JointStereo | block: 16 | subbands: 8 | allocation: Loudness | bitpool: 2..53)

Frame 145: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    146 1.360948       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVDTP    11     Sent ResponseAccept - SetConfiguration

Frame 146: 11 bytes on wire (88 bits), 11 bytes captured (88 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    147 1.375297       LiteonTe_d0:a5:b4 (laptop) localhost ()          AVDTP    12     Rcvd Command - Open - ACP SEID [1 - Audio Source]

Frame 147: 12 bytes on wire (96 bits), 12 bytes captured (96 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    148 1.375478       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVDTP    11     Sent ResponseAccept - Open

Frame 148: 11 bytes on wire (88 bits), 11 bytes captured (88 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVDTP Protocol

No.     Time           Source                Destination           Protocol Length Info
    149 1.391570       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 149: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    150 1.391576       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    17     Rcvd Connection Request (AVDTP, SCID: 0x0041)

Frame 150: 17 bytes on wire (136 bits), 17 bytes captured (136 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    151 1.391671       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Connection Response - Pending (SCID: 0x0041)

Frame 151: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    152 1.391842       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Connection Response - Success (SCID: 0x0041, DCID: 0x0041)

Frame 152: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    153 1.391858       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    28     Sent Configure Request (DCID: 0x0041)

Frame 153: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    154 1.407357       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 154: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    155 1.407365       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    28     Rcvd Configure Request (DCID: 0x0041)

Frame 155: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    156 1.407366       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    23     Rcvd Configure Response - Success (SCID: 0x0041)

Frame 156: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    157 1.407462       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    23     Sent Configure Response - Success (SCID: 0x0041)

Frame 157: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    158 1.423280       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 158: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    159 1.423287       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    17     Rcvd Connection Request (SDP, SCID: 0x0042)

Frame 159: 17 bytes on wire (136 bits), 17 bytes captured (136 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    160 1.423362       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Connection Response - Success (SCID: 0x0042, DCID: 0x0042)

Frame 160: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    161 1.423372       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    28     Sent Configure Request (DCID: 0x0042)

Frame 161: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    162 1.439537       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    17     Rcvd Connection Request (AVCTP-Control, SCID: 0x0043)

Frame 162: 17 bytes on wire (136 bits), 17 bytes captured (136 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    163 1.439543       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 163: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    164 1.439544       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    28     Rcvd Configure Request (DCID: 0x0042)

Frame 164: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    165 1.439545       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    23     Rcvd Configure Response - Success (SCID: 0x0042)

Frame 165: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    166 1.439638       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Connection Response - Pending (SCID: 0x0043)

Frame 166: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    167 1.439645       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    23     Sent Configure Response - Success (SCID: 0x0042)

Frame 167: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    168 1.440099       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    21     Sent Connection Response - Success (SCID: 0x0043, DCID: 0x0043)

Frame 168: 21 bytes on wire (168 bits), 21 bytes captured (168 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    169 1.440118       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    28     Sent Configure Request (DCID: 0x0043)

Frame 169: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    170 1.455541       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 170: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    171 1.455546       LiteonTe_d0:a5:b4 (laptop) localhost ()          SDP      29     Rcvd Service Search Attribute Request : L2CAP: Attribute Range (0x0000 - 0xffff) 

Frame 171: 29 bytes on wire (232 bits), 29 bytes captured (232 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth SDP Protocol

No.     Time           Source                Destination           Protocol Length Info
    172 1.455547       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 172: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    173 1.456233       localhost ()          LiteonTe_d0:a5:b4 (laptop) SDP      681    Sent Service Search Attribute Response (fragment)

Frame 173: 681 bytes on wire (5448 bits), 681 bytes captured (5448 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth SDP Protocol

No.     Time           Source                Destination           Protocol Length Info
    174 1.471346       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    28     Rcvd Configure Request (DCID: 0x0043)

Frame 174: 28 bytes on wire (224 bits), 28 bytes captured (224 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    175 1.471350       LiteonTe_d0:a5:b4 (laptop) localhost ()          L2CAP    23     Rcvd Configure Response - Success (SCID: 0x0043)

Frame 175: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    176 1.471445       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    23     Sent Configure Response - Success (SCID: 0x0043)

Frame 176: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    177 1.473512       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVRCP    23     Sent Vendor dependent: Status - GetCapabilities(Events Supported)

Frame 177: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVCTP Protocol
Bluetooth AVRCP Profile

No.     Time           Source                Destination           Protocol Length Info
    178 1.583101       LiteonTe_d0:a5:b4 (laptop) localhost ()          SDP      37     Rcvd Service Search Attribute Request : L2CAP: Attribute Range (0x0000 - 0xffff) 

Frame 178: 37 bytes on wire (296 bits), 37 bytes captured (296 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth SDP Protocol

No.     Time           Source                Destination           Protocol Length Info
    179 1.583104       controller            host                  HCI_EVT  8      Rcvd Number of Completed Packets

Frame 179: 8 bytes on wire (64 bits), 8 bytes captured (64 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Number of Completed Packets

No.     Time           Source                Destination           Protocol Length Info
    180 1.583105       LiteonTe_d0:a5:b4 (laptop) localhost ()          AVRCP    23     Rcvd Vendor dependent: Status - GetCapabilities(Events Supported)

Frame 180: 23 bytes on wire (184 bits), 23 bytes captured (184 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVCTP Protocol
Bluetooth AVRCP Profile

No.     Time           Source                Destination           Protocol Length Info
    181 1.583105       LiteonTe_d0:a5:b4 (laptop) localhost ()          AVRCP    29     Rcvd Vendor dependent: Stable - GetCapabilities(Events Supported) - Count: 5

Frame 181: 29 bytes on wire (232 bits), 29 bytes captured (232 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVCTP Protocol
Bluetooth AVRCP Profile

No.     Time           Source                Destination           Protocol Length Info
    182 1.583207       localhost ()          LiteonTe_d0:a5:b4 (laptop) SDP      681    Sent Service Search Attribute Response (fragment)

Frame 182: 681 bytes on wire (5448 bits), 681 bytes captured (5448 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth SDP Protocol

No.     Time           Source                Destination           Protocol Length Info
    183 1.583213       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVRCP    32     Sent Vendor dependent: Stable - GetCapabilities(Events Supported) - Count: 8

Frame 183: 32 bytes on wire (256 bits), 32 bytes captured (256 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVCTP Protocol
Bluetooth AVRCP Profile

No.     Time           Source                Destination           Protocol Length Info
    184 1.583273       localhost ()          LiteonTe_d0:a5:b4 (laptop) L2CAP    17     Sent Connection Request (AVCTP-Browsing, SCID: 0x0044)

Frame 184: 17 bytes on wire (136 bits), 17 bytes captured (136 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol

No.     Time           Source                Destination           Protocol Length Info
    185 1.583300       localhost ()          LiteonTe_d0:a5:b4 (laptop) AVRCP    27     Sent Vendor dependent: Notify - RegisterNotification - PlayerApplicationSettingChanged

Frame 185: 27 bytes on wire (216 bits), 27 bytes captured (216 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI ACL Packet
Bluetooth L2CAP Protocol
Bluetooth AVCTP Protocol
Bluetooth AVRCP Profile

No.     Time           Source                Destination           Protocol Length Info
    186 1.679437       controller            host                  HCI_EVT  247    Rcvd Vendor-Specific

Frame 186: 247 bytes on wire (1976 bits), 247 bytes captured (1976 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Vendor-Specific

No.     Time           Source                Destination           Protocol Length Info
    187 1.695380       controller            host                  HCI_EVT  247    Rcvd Vendor-Specific

Frame 187: 247 bytes on wire (1976 bits), 247 bytes captured (1976 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Vendor-Specific

No.     Time           Source                Destination           Protocol Length Info
    188 1.711114       controller            host                  HCI_EVT  247    Rcvd Vendor-Specific

Frame 188: 247 bytes on wire (1976 bits), 247 bytes captured (1976 bits) on interface bluetooth1, id 0
Bluetooth
Bluetooth HCI H4
Bluetooth HCI Event - Vendor-Specific
```
