# LinkrealmsTinkering
Tinkering with Linkrealms


Interesting info found in update.exe

00471699   . BA 50174700                                        MOV EDX,update.00471750                       ;  ASCII " -UPDATED"
0047169E   . E8 CD31F9FF                                        CALL update.00404870
004716A3   . 8B45 EC                                            MOV EAX,DWORD PTR SS:[EBP-14]
004716A6   . E8 BD33F9FF                                        CALL update.00404A68
004716AB   . 50                                                 PUSH EAX
004716AC   . 8D55 E4                                            LEA EDX,DWORD PTR SS:[EBP-1C]
004716AF   . 33C0                                               XOR EAX,EAX
004716B1   . E8 8E13F9FF                                        CALL update.00402A44
004716B6   . 8B45 E4                                            MOV EAX,DWORD PTR SS:[EBP-1C]
004716B9   . 8D55 E8                                            LEA EDX,DWORD PTR SS:[EBP-18]
004716BC   . E8 E378F9FF                                        CALL update.00408FA4
004716C1   . 8D45 E8                                            LEA EAX,DWORD PTR SS:[EBP-18]
004716C4   . BA 64174700                                        MOV EDX,update.00471764                       ;  ASCII "PatchNews.exe"
004716C9   . E8 A231F9FF                                        CALL update.00404870
004716CE   . 8B45 E8                                            MOV EAX,DWORD PTR SS:[EBP-18]
004716D1   . E8 9233F9FF                                        CALL update.00404A68
004716D6   . 50                                                 PUSH EAX                                      ; |FileName
004716D7   . 68 74174700                                        PUSH update.00471774                          ; |Operation = "open"
004716DC   . 6A 00                                              PUSH 0                                        ; |hWnd = NULL
004716DE   . E8 09D0F9FF                                        CALL <JMP.&shell32.ShellExecuteA>             ; \ShellExecuteA
004716E3   . 33C0                                               XOR EAX,EAX
004716E5   . 5A                                                 POP EDX
004716E6   . 59                                                 POP ECX
004716E7   . 59                                                 POP ECX
004716E8   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
004716EB   . EB 2F                                              JMP SHORT update.0047171C
004716ED   .^E9 AE26F9FF                                        JMP update.00403DA0
004716F2     01                                                 DB 01
004716F3     00                                                 DB 00
004716F4     00                                                 DB 00
004716F5     00                                                 DB 00
004716F6   . B0784000                                           DD update.004078B0
004716FA   . FE164700                                           DD update.004716FE
004716FE   . 8945 F8                                            MOV DWORD PTR SS:[EBP-8],EAX
00471701   . 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00471703   . 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]                  ; |
00471706   . 8B40 04                                            MOV EAX,DWORD PTR DS:[EAX+4]                  ; |
00471709   . 66:8B0D 7C174700                                   MOV CX,WORD PTR DS:[47177C]                   ; |
00471710   . B2 01                                              MOV DL,1                                      ; |
00471712   . E8 592FFEFF                                        CALL update.00454670                          ; \update.00454670
00471717   . E8 C028F9FF                                        CALL update.00403FDC
0047171C   > 33C0                                               XOR EAX,EAX
0047171E   . 5A                                                 POP EDX
0047171F   . 59                                                 POP ECX
00471720   . 59                                                 POP ECX
00471721   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00471724   . 68 3E174700                                        PUSH update.0047173E
00471729   > 8D45 E4                                            LEA EAX,DWORD PTR SS:[EBP-1C]
0047172C   . BA 05000000                                        MOV EDX,5
00471731   . E8 962EF9FF                                        CALL update.004045CC
00471736   . C3                                                 RETN
00471737   .^E9 EC27F9FF                                        JMP update.00403F28
0047173C   .^EB EB                                              JMP SHORT update.00471729
0047173E   . 5F                                                 POP EDI
0047173F   . 5E                                                 POP ESI
00471740   . 5B                                                 POP EBX
00471741   . 8BE5                                               MOV ESP,EBP
00471743   . 5D                                                 POP EBP
00471744   . C3                                                 RETN
00471745     00                                                 DB 00
00471746     00                                                 DB 00
00471747     00                                                 DB 00
00471748   . FFFFFFFF                                           DD FFFFFFFF
0047174C   . 09000000                                           DD 00000009
00471750   . 20 2D 55 50 44 41 54 45 44 00                      ASCII " -UPDATED",0
0047175A     00                                                 DB 00
0047175B     00                                                 DB 00
0047175C   . FFFFFFFF                                           DD FFFFFFFF
00471760   . 0D000000                                           DD 0000000D
00471764   . 50 61 74 63 68 4E 65 77 73 2E 65 78 65 00          ASCII "PatchNews.exe",0
00471772     00                                                 DB 00
00471773     00                                                 DB 00
00471774   . 6F 70 65 6E 00                                     ASCII "open",0
00471779     00                                                 DB 00
0047177A     00                                                 DB 00
0047177B     00                                                 DB 00
0047177C   . 0400                                               DW 0004
0047177E     00                                                 DB 00
0047177F     00                                                 DB 00
00471780  /. 55                                                 PUSH EBP
00471781  |. 8BEC                                               MOV EBP,ESP
00471783  |. 83C4 F4                                            ADD ESP,-0C
00471786  |. 884D FB                                            MOV BYTE PTR SS:[EBP-5],CL
00471789  |. 8955 F4                                            MOV DWORD PTR SS:[EBP-C],EDX
0047178C  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
0047178F  |. 807D FB 02                                         CMP BYTE PTR SS:[EBP-5],2
00471793  |. 75 13                                              JNZ SHORT update.004717A8
00471795  |. BA B8174700                                        MOV EDX,update.004717B8                       ;  ASCII "Checking for updates..."
0047179A  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047179D  |. 8B80 08030000                                      MOV EAX,DWORD PTR DS:[EAX+308]
004717A3  |. E8 5C13FCFF                                        CALL update.00432B04
004717A8  |> 8BE5                                               MOV ESP,EBP
004717AA  |. 5D                                                 POP EBP
004717AB  \. C2 0400                                            RETN 4
004717AE     00                                                 DB 00
004717AF     00                                                 DB 00
004717B0   . FFFFFFFF                                           DD FFFFFFFF
004717B4   . 17000000                                           DD 00000017
004717B8   . 43 68 65 63 6B 69 6E 67 20 66 6F 72 20 75 70 64    ASCII "Checking for upd"
004717C8   . 61 74 65 73 2E 2E 2E 00                            ASCII "ates...",0
004717D0   $ 55                                                 PUSH EBP
004717D1   . 8BEC                                               MOV EBP,ESP
004717D3   . 81C4 1CFEFFFF                                      ADD ESP,-1E4
004717D9   . 53                                                 PUSH EBX
004717DA   . 56                                                 PUSH ESI
004717DB   . 57                                                 PUSH EDI
004717DC   . 33D2                                               XOR EDX,EDX
004717DE   . 8995 20FEFFFF                                      MOV DWORD PTR SS:[EBP-1E0],EDX
004717E4   . 8995 1CFEFFFF                                      MOV DWORD PTR SS:[EBP-1E4],EDX
004717EA   . 8995 28FEFFFF                                      MOV DWORD PTR SS:[EBP-1D8],EDX
004717F0   . 8995 24FEFFFF                                      MOV DWORD PTR SS:[EBP-1DC],EDX
004717F6   . 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
004717F9   . 33C0                                               XOR EAX,EAX
004717FB   . 55                                                 PUSH EBP
004717FC   . 68 65194700                                        PUSH update.00471965
00471801   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
00471804   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00471807   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047180A   . 05 24030000                                        ADD EAX,324
0047180F   . E8 942DF9FF                                        CALL update.004045A8
00471814   . 33C0                                               XOR EAX,EAX
00471816   . 55                                                 PUSH EBP
00471817   . 68 19194700                                        PUSH update.00471919
0047181C   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
0047181F   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00471822   . 8D95 24FEFFFF                                      LEA EDX,DWORD PTR SS:[EBP-1DC]
00471828   . 33C0                                               XOR EAX,EAX
0047182A   . E8 1512F9FF                                        CALL update.00402A44
0047182F   . 8B85 24FEFFFF                                      MOV EAX,DWORD PTR SS:[EBP-1DC]
00471835   . 8D95 28FEFFFF                                      LEA EDX,DWORD PTR SS:[EBP-1D8]
0047183B   . E8 6477F9FF                                        CALL update.00408FA4
00471840   . 8D85 28FEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1D8]
00471846   . BA 7C194700                                        MOV EDX,update.0047197C                       ;  ASCII "version.ini"
0047184B   . E8 2030F9FF                                        CALL update.00404870
00471850   . 8B85 28FEFFFF                                      MOV EAX,DWORD PTR SS:[EBP-1D8]
00471856   . E8 A176F9FF                                        CALL update.00408EFC
0047185B   . 84C0                                               TEST AL,AL
0047185D   . 0F84 97000000                                      JE update.004718FA
00471863   . 8D95 1CFEFFFF                                      LEA EDX,DWORD PTR SS:[EBP-1E4]
00471869   . 33C0                                               XOR EAX,EAX
0047186B   . E8 D411F9FF                                        CALL update.00402A44
00471870   . 8B85 1CFEFFFF                                      MOV EAX,DWORD PTR SS:[EBP-1E4]
00471876   . 8D95 20FEFFFF                                      LEA EDX,DWORD PTR SS:[EBP-1E0]
0047187C   . E8 2377F9FF                                        CALL update.00408FA4
00471881   . 8D85 20FEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1E0]
00471887   . BA 7C194700                                        MOV EDX,update.0047197C                       ;  ASCII "version.ini"
0047188C   . E8 DF2FF9FF                                        CALL update.00404870
00471891   . 8B95 20FEFFFF                                      MOV EDX,DWORD PTR SS:[EBP-1E0]
00471897   . 8D85 2CFEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1D4]
0047189D   . E8 4E15F9FF                                        CALL update.00402DF0
004718A2   . 8D85 2CFEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1D4]
004718A8   . E8 DF12F9FF                                        CALL update.00402B8C
004718AD   . 33C0                                               XOR EAX,EAX
004718AF   . 55                                                 PUSH EBP
004718B0   . 68 F3184700                                        PUSH update.004718F3
004718B5   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
004718B8   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
004718BB   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004718BE   . 8D90 24030000                                      LEA EDX,DWORD PTR DS:[EAX+324]
004718C4   . 8D85 2CFEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1D4]
004718CA   . E8 9918F9FF                                        CALL update.00403168
004718CF   . 8D85 2CFEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1D4]
004718D5   . E8 FA18F9FF                                        CALL update.004031D4
004718DA   . 33C0                                               XOR EAX,EAX
004718DC   . 5A                                                 POP EDX
004718DD   . 59                                                 POP ECX
004718DE   . 59                                                 POP ECX
004718DF   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
004718E2   . 68 0F194700                                        PUSH update.0047190F
004718E7   > 8D85 2CFEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1D4]
004718ED   . E8 BA15F9FF                                        CALL update.00402EAC
004718F2   . C3                                                 RETN
004718F3   .^E9 3026F9FF                                        JMP update.00403F28
004718F8   .^EB ED                                              JMP SHORT update.004718E7
004718FA   > 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
004718FC   . 66:8B0D 88194700                                   MOV CX,WORD PTR DS:[471988]                   ; |
00471903   . B2 01                                              MOV DL,1                                      ; |
00471905   . B8 94194700                                        MOV EAX,update.00471994                       ; |ASCII "Could not load version.ini.  Patch failed, please reinstall."
0047190A   . E8 612DFEFF                                        CALL update.00454670                          ; \update.00454670
0047190F   . 33C0                                               XOR EAX,EAX
00471911   . 5A                                                 POP EDX
00471912   . 59                                                 POP ECX
00471913   . 59                                                 POP ECX
00471914   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00471917   . EB 2E                                              JMP SHORT update.00471947
00471919   .^E9 8224F9FF                                        JMP update.00403DA0
0047191E     01                                                 DB 01
0047191F     00                                                 DB 00
00471920     00                                                 DB 00
00471921     00                                                 DB 00
00471922   . B0784000                                           DD update.004078B0
00471926   . 2A194700                                           DD update.0047192A
0047192A   . 8945 F8                                            MOV DWORD PTR SS:[EBP-8],EAX
0047192D   . 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
0047192F   . 66:8B0D 88194700                                   MOV CX,WORD PTR DS:[471988]                   ; |
00471936   . B2 01                                              MOV DL,1                                      ; |
00471938   . B8 94194700                                        MOV EAX,update.00471994                       ; |ASCII "Could not load version.ini.  Patch failed, please reinstall."
0047193D   . E8 2E2DFEFF                                        CALL update.00454670                          ; \update.00454670
00471942   . E8 9526F9FF                                        CALL update.00403FDC
00471947   > 33C0                                               XOR EAX,EAX
00471949   . 5A                                                 POP EDX
0047194A   . 59                                                 POP ECX
0047194B   . 59                                                 POP ECX
0047194C   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
0047194F   . 68 6C194700                                        PUSH update.0047196C
00471954   > 8D85 1CFEFFFF                                      LEA EAX,DWORD PTR SS:[EBP-1E4]
0047195A   . BA 04000000                                        MOV EDX,4
0047195F   . E8 682CF9FF                                        CALL update.004045CC
00471964   . C3                                                 RETN
00471965   .^E9 BE25F9FF                                        JMP update.00403F28
0047196A   .^EB E8                                              JMP SHORT update.00471954
0047196C   . 5F                                                 POP EDI
0047196D   . 5E                                                 POP ESI
0047196E   . 5B                                                 POP EBX
0047196F   . 8BE5                                               MOV ESP,EBP
00471971   . 5D                                                 POP EBP
00471972   . C3                                                 RETN
00471973     00                                                 DB 00
00471974   . FFFFFFFF                                           DD FFFFFFFF
00471978   . 0B000000                                           DD 0000000B
0047197C   . 76 65 72 73 69 6F 6E 2E 69 6E 69 00                ASCII "version.ini",0
00471988   . 0400                                               DW 0004
0047198A     00                                                 DB 00
0047198B     00                                                 DB 00
0047198C   . FFFFFFFF                                           DD FFFFFFFF
00471990   . 3C000000                                           DD 0000003C
00471994   . 43 6F 75 6C 64 20 6E 6F 74 20 6C 6F 61 64 20 76    ASCII "Could not load v"
004719A4   . 65 72 73 69 6F 6E 2E 69 6E 69 2E 20 20 50 61 74    ASCII "ersion.ini.  Pat"
004719B4   . 63 68 20 66 61 69 6C 65 64 2C 20 70 6C 65 61 73    ASCII "ch failed, pleas"
004719C4   . 65 20 72 65 69 6E 73 74 61 6C 6C 2E 00             ASCII "e reinstall.",0
004719D1     00                                                 DB 00
004719D2     00                                                 DB 00
004719D3     00                                                 DB 00
004719D4   . 55                                                 PUSH EBP
004719D5   . 8BEC                                               MOV EBP,ESP
004719D7   . B9 11000000                                        MOV ECX,11
004719DC   > 6A 00                                              PUSH 0
004719DE   . 6A 00                                              PUSH 0
004719E0   . 49                                                 DEC ECX
004719E1   .^75 F9                                              JNZ SHORT update.004719DC
004719E3   . 53                                                 PUSH EBX
004719E4   . 56                                                 PUSH ESI
004719E5   . 57                                                 PUSH EDI
004719E6   . 8955 D0                                            MOV DWORD PTR SS:[EBP-30],EDX
004719E9   . 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
004719EC   . 33C0                                               XOR EAX,EAX
004719EE   . 55                                                 PUSH EBP
004719EF   . 68 31204700                                        PUSH update.00472031
004719F4   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
004719F7   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
004719FA   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004719FD   . 8B80 10030000                                      MOV EAX,DWORD PTR DS:[EAX+310]
00471A03   . 33D2                                               XOR EDX,EDX
00471A05   . E8 DA7FFBFF                                        CALL update.004299E4
00471A0A   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471A0D   . 8B80 04030000                                      MOV EAX,DWORD PTR DS:[EAX+304]
00471A13   . B2 01                                              MOV DL,1
00471A15   . 8B08                                               MOV ECX,DWORD PTR DS:[EAX]
00471A17   . FF51 64                                            CALL DWORD PTR DS:[ECX+64]
00471A1A   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471A1D   . E8 AEFDFFFF                                        CALL update.004717D0
00471A22   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471A25   . 83B8 24030000 00                                   CMP DWORD PTR DS:[EAX+324],0
00471A2C   . 0F84 C6050000                                      JE update.00471FF8
00471A32   . A1 205A4700                                        MOV EAX,DWORD PTR DS:[475A20]
00471A37   . 8B00                                               MOV EAX,DWORD PTR DS:[EAX]
00471A39   . E8 1605FEFF                                        CALL update.00451F54
00471A3E   . 8D45 F4                                            LEA EAX,DWORD PTR SS:[EBP-C]
00471A41   . E8 622BF9FF                                        CALL update.004045A8
00471A46   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471A49   . 80B8 30030000 00                                   CMP BYTE PTR DS:[EAX+330],0
00471A50   . 0F84 2B020000                                      JE update.00471C81
00471A56   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471A59   . C680 30030000 00                                   MOV BYTE PTR DS:[EAX+330],0
00471A60   . 33C0                                               XOR EAX,EAX
00471A62   . 55                                                 PUSH EBP
00471A63   . 68 441C4700                                        PUSH update.00471C44
00471A68   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
00471A6B   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00471A6E   . 8D4D F8                                            LEA ECX,DWORD PTR SS:[EBP-8]
00471A71   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471A74   . 8B80 0C030000                                      MOV EAX,DWORD PTR DS:[EAX+30C]
00471A7A   . BA 48204700                                        MOV EDX,update.00472048                       ;  ASCII "http://patch.linkrealms.com/patch/patch.txt"
00471A7F   . E8 70C9FFFF                                        CALL update.0046E3F4
00471A84   . 837D F8 00                                         CMP DWORD PTR SS:[EBP-8],0
00471A88   . 0F84 93010000                                      JE update.00471C21
00471A8E   . 33C0                                               XOR EAX,EAX
00471A90   . 8945 E8                                            MOV DWORD PTR SS:[EBP-18],EAX
00471A93   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471A96   . 8B80 34030000                                      MOV EAX,DWORD PTR DS:[EAX+334]
00471A9C   . 8B55 F8                                            MOV EDX,DWORD PTR SS:[EBP-8]
00471A9F   . 8B08                                               MOV ECX,DWORD PTR DS:[EAX]
00471AA1   . FF51 2C                                            CALL DWORD PTR DS:[ECX+2C]
00471AA4   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471AA7   . 8B80 34030000                                      MOV EAX,DWORD PTR DS:[EAX+334]
00471AAD   . 8B10                                               MOV EDX,DWORD PTR DS:[EAX]
00471AAF   . FF52 14                                            CALL DWORD PTR DS:[EDX+14]
00471AB2   . 48                                                 DEC EAX
00471AB3   . 85C0                                               TEST EAX,EAX
00471AB5   . 0F8C 80000000                                      JL update.00471B3B
00471ABB   . 40                                                 INC EAX
00471ABC   . 8945 E0                                            MOV DWORD PTR SS:[EBP-20],EAX
00471ABF   . C745 EC 00000000                                   MOV DWORD PTR SS:[EBP-14],0
00471AC6   > 8D4D CC                                            LEA ECX,DWORD PTR SS:[EBP-34]
00471AC9   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471ACC   . 8B80 34030000                                      MOV EAX,DWORD PTR DS:[EAX+334]
00471AD2   . 8B55 EC                                            MOV EDX,DWORD PTR SS:[EBP-14]
00471AD5   . 8B18                                               MOV EBX,DWORD PTR DS:[EAX]
00471AD7   . FF53 0C                                            CALL DWORD PTR DS:[EBX+C]
00471ADA   . 837D CC 00                                         CMP DWORD PTR SS:[EBP-34],0
00471ADE   . 74 53                                              JE SHORT update.00471B33
00471AE0   . 8D4D C8                                            LEA ECX,DWORD PTR SS:[EBP-38]
00471AE3   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471AE6   . 8B80 34030000                                      MOV EAX,DWORD PTR DS:[EAX+334]
00471AEC   . 8B55 EC                                            MOV EDX,DWORD PTR SS:[EBP-14]
00471AEF   . 8B18                                               MOV EBX,DWORD PTR DS:[EAX]
00471AF1   . FF53 0C                                            CALL DWORD PTR DS:[EBX+C]
00471AF4   . 8B45 C8                                            MOV EAX,DWORD PTR SS:[EBP-38]
00471AF7   . 8D55 F0                                            LEA EDX,DWORD PTR SS:[EBP-10]
00471AFA   . B1 2C                                              MOV CL,2C
00471AFC   . E8 BBF9FFFF                                        CALL update.004714BC
00471B01   . 837D F4 00                                         CMP DWORD PTR SS:[EBP-C],0
00471B05   . 75 23                                              JNZ SHORT update.00471B2A
00471B07   . 8B45 F0                                            MOV EAX,DWORD PTR SS:[EBP-10]
00471B0A   . 8B00                                               MOV EAX,DWORD PTR DS:[EAX]
00471B0C   . 8B55 FC                                            MOV EDX,DWORD PTR SS:[EBP-4]
00471B0F   . 8B92 24030000                                      MOV EDX,DWORD PTR DS:[EDX+324]
00471B15   . E8 9A2EF9FF                                        CALL update.004049B4
00471B1A   . 75 0E                                              JNZ SHORT update.00471B2A
00471B1C   . 8D45 F4                                            LEA EAX,DWORD PTR SS:[EBP-C]
00471B1F   . 8B55 F0                                            MOV EDX,DWORD PTR SS:[EBP-10]
00471B22   . 8B52 04                                            MOV EDX,DWORD PTR DS:[EDX+4]
00471B25   . E8 162BF9FF                                        CALL update.00404640
00471B2A   > 837D F4 00                                         CMP DWORD PTR SS:[EBP-C],0
00471B2E   . 74 03                                              JE SHORT update.00471B33
00471B30   . FF45 E8                                            INC DWORD PTR SS:[EBP-18]
00471B33   > FF45 EC                                            INC DWORD PTR SS:[EBP-14]
00471B36   . FF4D E0                                            DEC DWORD PTR SS:[EBP-20]
00471B39   .^75 8B                                              JNZ SHORT update.00471AC6
00471B3B   > 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471B3E   . 8B55 E8                                            MOV EDX,DWORD PTR SS:[EBP-18]
00471B41   . 8990 2C030000                                      MOV DWORD PTR DS:[EAX+32C],EDX
00471B47   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471B4A   . 80B8 3C030000 00                                   CMP BYTE PTR DS:[EAX+33C],0
00471B51   . 0F84 E0000000                                      JE update.00471C37
00471B57   . 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00471B59   . 66:8B0D 74204700                                   MOV CX,WORD PTR DS:[472074]                   ; |
00471B60   . 33D2                                               XOR EDX,EDX                                   ; |
00471B62   . B8 80204700                                        MOV EAX,update.00472080                       ; |ASCII "Patch cancelled.  Your game client may be out of date and not function properly."
00471B67   . E8 042BFEFF                                        CALL update.00454670                          ; \update.00454670
00471B6C   . 33C0                                               XOR EAX,EAX
00471B6E   . 55                                                 PUSH EBP
00471B6F   . 68 E31B4700                                        PUSH update.00471BE3
00471B74   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
00471B77   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00471B7A   . 6A 05                                              PUSH 5
00471B7C   . 8D55 C0                                            LEA EDX,DWORD PTR SS:[EBP-40]
00471B7F   . 33C0                                               XOR EAX,EAX
00471B81   . E8 BE0EF9FF                                        CALL update.00402A44
00471B86   . 8B45 C0                                            MOV EAX,DWORD PTR SS:[EBP-40]
00471B89   . 8D55 C4                                            LEA EDX,DWORD PTR SS:[EBP-3C]
00471B8C   . E8 1374F9FF                                        CALL update.00408FA4
00471B91   . 8B45 C4                                            MOV EAX,DWORD PTR SS:[EBP-3C]
00471B94   . E8 CF2EF9FF                                        CALL update.00404A68
00471B99   . 50                                                 PUSH EAX
00471B9A   . A1 D0594700                                        MOV EAX,DWORD PTR DS:[4759D0]
00471B9F   . 8B00                                               MOV EAX,DWORD PTR DS:[EAX]
00471BA1   . 50                                                 PUSH EAX
00471BA2   . 8D55 B8                                            LEA EDX,DWORD PTR SS:[EBP-48]
00471BA5   . 33C0                                               XOR EAX,EAX
00471BA7   . E8 980EF9FF                                        CALL update.00402A44
00471BAC   . 8B45 B8                                            MOV EAX,DWORD PTR SS:[EBP-48]
00471BAF   . 8D55 BC                                            LEA EDX,DWORD PTR SS:[EBP-44]
00471BB2   . E8 ED73F9FF                                        CALL update.00408FA4
00471BB7   . 8D45 BC                                            LEA EAX,DWORD PTR SS:[EBP-44]
00471BBA   . BA DC204700                                        MOV EDX,update.004720DC                       ;  ASCII "linkrealms.exe"
00471BBF   . E8 AC2CF9FF                                        CALL update.00404870
00471BC4   . 8B45 BC                                            MOV EAX,DWORD PTR SS:[EBP-44]
00471BC7   . E8 9C2EF9FF                                        CALL update.00404A68
00471BCC   . 50                                                 PUSH EAX                                      ; |FileName
00471BCD   . 68 EC204700                                        PUSH update.004720EC                          ; |Operation = "open"
00471BD2   . 6A 00                                              PUSH 0                                        ; |hWnd = NULL
00471BD4   . E8 13CBF9FF                                        CALL <JMP.&shell32.ShellExecuteA>             ; \ShellExecuteA
00471BD9   . 33C0                                               XOR EAX,EAX
00471BDB   . 5A                                                 POP EDX
00471BDC   . 59                                                 POP ECX
00471BDD   . 59                                                 POP ECX
00471BDE   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00471BE1   . EB 2F                                              JMP SHORT update.00471C12
00471BE3   .^E9 B821F9FF                                        JMP update.00403DA0
00471BE8     01                                                 DB 01
00471BE9     00                                                 DB 00
00471BEA     00                                                 DB 00
00471BEB     00                                                 DB 00
00471BEC   . B0784000                                           DD update.004078B0
00471BF0   . F41B4700                                           DD update.00471BF4
00471BF4   . 8945 DC                                            MOV DWORD PTR SS:[EBP-24],EAX
00471BF7   . 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00471BF9   . 8B45 DC                                            MOV EAX,DWORD PTR SS:[EBP-24]                 ; |
00471BFC   . 8B40 04                                            MOV EAX,DWORD PTR DS:[EAX+4]                  ; |
00471BFF   . 66:8B0D 74204700                                   MOV CX,WORD PTR DS:[472074]                   ; |
00471C06   . B2 01                                              MOV DL,1                                      ; |
00471C08   . E8 632AFEFF                                        CALL update.00454670                          ; \update.00454670
00471C0D   . E8 CA23F9FF                                        CALL update.00403FDC
00471C12   > 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471C15   . E8 1EFAFFFF                                        CALL update.00471638
00471C1A   . E8 1528F9FF                                        CALL update.00404434
00471C1F   . EB 16                                              JMP SHORT update.00471C37
00471C21   > B9 FC204700                                        MOV ECX,update.004720FC                       ;  ASCII "Empty List"
00471C26   . B2 01                                              MOV DL,1
00471C28   . A1 34144700                                        MOV EAX,DWORD PTR DS:[471434]
00471C2D   . E8 52A8F9FF                                        CALL update.0040C484
00471C32   . E8 2923F9FF                                        CALL update.00403F60
00471C37   > 33C0                                               XOR EAX,EAX
00471C39   . 5A                                                 POP EDX
00471C3A   . 59                                                 POP ECX
00471C3B   . 59                                                 POP ECX
00471C3C   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00471C3F   . E9 A9000000                                        JMP update.00471CED
00471C44   .^E9 5721F9FF                                        JMP update.00403DA0
00471C49     01                                                 DB 01
00471C4A     00                                                 DB 00
00471C4B     00                                                 DB 00
00471C4C     00                                                 DB 00
00471C4D   . B0784000                                           DD update.004078B0
00471C51   . 551C4700                                           DD update.00471C55
00471C55   . 8945 D8                                            MOV DWORD PTR SS:[EBP-28],EAX
00471C58   . 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00471C5A   . 66:8B0D 74204700                                   MOV CX,WORD PTR DS:[472074]                   ; |
00471C61   . 33D2                                               XOR EDX,EDX                                   ; |
00471C63   . B8 10214700                                        MOV EAX,update.00472110                       ; |ASCII "Could not retrieve patch information.
The patch server may be temporarily unavailable."
00471C68   . E8 032AFEFF                                        CALL update.00454670                          ; \update.00454670
00471C6D   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471C70   . E8 C3F9FFFF                                        CALL update.00471638
00471C75   . E8 BA27F9FF                                        CALL update.00404434
00471C7A   . E8 5D23F9FF                                        CALL update.00403FDC
00471C7F   . EB 6C                                              JMP SHORT update.00471CED
00471C81   > 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471C84   . 8B80 34030000                                      MOV EAX,DWORD PTR DS:[EAX+334]
00471C8A   . 8B10                                               MOV EDX,DWORD PTR DS:[EAX]
00471C8C   . FF52 14                                            CALL DWORD PTR DS:[EDX+14]
00471C8F   . 48                                                 DEC EAX
00471C90   . 85C0                                               TEST EAX,EAX
00471C92   . 7C 59                                              JL SHORT update.00471CED
00471C94   . 40                                                 INC EAX
00471C95   . 8945 E0                                            MOV DWORD PTR SS:[EBP-20],EAX
00471C98   . C745 EC 00000000                                   MOV DWORD PTR SS:[EBP-14],0
00471C9F   > 8D4D B4                                            LEA ECX,DWORD PTR SS:[EBP-4C]
00471CA2   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471CA5   . 8B80 34030000                                      MOV EAX,DWORD PTR DS:[EAX+334]
00471CAB   . 8B55 EC                                            MOV EDX,DWORD PTR SS:[EBP-14]
00471CAE   . 8B18                                               MOV EBX,DWORD PTR DS:[EAX]
00471CB0   . FF53 0C                                            CALL DWORD PTR DS:[EBX+C]
00471CB3   . 8B45 B4                                            MOV EAX,DWORD PTR SS:[EBP-4C]
00471CB6   . 8D55 F0                                            LEA EDX,DWORD PTR SS:[EBP-10]
00471CB9   . B1 2C                                              MOV CL,2C
00471CBB   . E8 FCF7FFFF                                        CALL update.004714BC
00471CC0   . 8B45 F0                                            MOV EAX,DWORD PTR SS:[EBP-10]
00471CC3   . 8B00                                               MOV EAX,DWORD PTR DS:[EAX]
00471CC5   . 8B55 FC                                            MOV EDX,DWORD PTR SS:[EBP-4]
00471CC8   . 8B92 24030000                                      MOV EDX,DWORD PTR DS:[EDX+324]
00471CCE   . E8 E12CF9FF                                        CALL update.004049B4
00471CD3   . 75 10                                              JNZ SHORT update.00471CE5
00471CD5   . 8D45 F4                                            LEA EAX,DWORD PTR SS:[EBP-C]
00471CD8   . 8B55 F0                                            MOV EDX,DWORD PTR SS:[EBP-10]
00471CDB   . 8B52 04                                            MOV EDX,DWORD PTR DS:[EDX+4]
00471CDE   . E8 5D29F9FF                                        CALL update.00404640
00471CE3   . EB 08                                              JMP SHORT update.00471CED
00471CE5   > FF45 EC                                            INC DWORD PTR SS:[EBP-14]
00471CE8   . FF4D E0                                            DEC DWORD PTR SS:[EBP-20]
00471CEB   .^75 B2                                              JNZ SHORT update.00471C9F
00471CED   > 837D F4 00                                         CMP DWORD PTR SS:[EBP-C],0
00471CF1   . 0F84 F4020000                                      JE update.00471FEB
00471CF7   . 8D55 AC                                            LEA EDX,DWORD PTR SS:[EBP-54]
00471CFA   . 33C0                                               XOR EAX,EAX
00471CFC   . E8 430DF9FF                                        CALL update.00402A44
00471D01   . 8B45 AC                                            MOV EAX,DWORD PTR SS:[EBP-54]
00471D04   . 8D55 B0                                            LEA EDX,DWORD PTR SS:[EBP-50]
00471D07   . E8 9872F9FF                                        CALL update.00408FA4
00471D0C   . 8D45 B0                                            LEA EAX,DWORD PTR SS:[EBP-50]
00471D0F   . BA 70214700                                        MOV EDX,update.00472170                       ;  ASCII "patch_update.exe"
00471D14   . E8 572BF9FF                                        CALL update.00404870
00471D19   . 8B45 B0                                            MOV EAX,DWORD PTR SS:[EBP-50]
00471D1C   . E8 DB71F9FF                                        CALL update.00408EFC
00471D21   . 84C0                                               TEST AL,AL
00471D23   . 0F85 C2020000                                      JNZ update.00471FEB
00471D29   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471D2C   . FF80 28030000                                      INC DWORD PTR DS:[EAX+328]
00471D32   . 68 8C214700                                        PUSH update.0047218C                          ;  ASCII "Downloading patch "
00471D37   . 8D55 A4                                            LEA EDX,DWORD PTR SS:[EBP-5C]
00471D3A   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471D3D   . 8B80 28030000                                      MOV EAX,DWORD PTR DS:[EAX+328]
00471D43   . E8 986CF9FF                                        CALL update.004089E0
00471D48   . FF75 A4                                            PUSH DWORD PTR SS:[EBP-5C]
00471D4B   . 68 A8214700                                        PUSH update.004721A8                          ;  ASCII " of "
00471D50   . 8D55 A0                                            LEA EDX,DWORD PTR SS:[EBP-60]
00471D53   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471D56   . 8B80 2C030000                                      MOV EAX,DWORD PTR DS:[EAX+32C]
00471D5C   . E8 7F6CF9FF                                        CALL update.004089E0
00471D61   . FF75 A0                                            PUSH DWORD PTR SS:[EBP-60]
00471D64   . 68 B8214700                                        PUSH update.004721B8                          ;  ASCII "..."
00471D69   . 8D45 A8                                            LEA EAX,DWORD PTR SS:[EBP-58]
00471D6C   . BA 05000000                                        MOV EDX,5
00471D71   . E8 B22BF9FF                                        CALL update.00404928
00471D76   . 8B55 A8                                            MOV EDX,DWORD PTR SS:[EBP-58]
00471D79   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471D7C   . 8B80 08030000                                      MOV EAX,DWORD PTR DS:[EAX+308]
00471D82   . E8 7D0DFCFF                                        CALL update.00432B04
00471D87   . B2 01                                              MOV DL,1
00471D89   . A1 C0344100                                        MOV EAX,DWORD PTR DS:[4134C0]
00471D8E   . E8 111AF9FF                                        CALL update.004037A4
00471D93   . 8945 E4                                            MOV DWORD PTR SS:[EBP-1C],EAX
00471D96   . 33C0                                               XOR EAX,EAX
00471D98   . 55                                                 PUSH EBP
00471D99   . 68 E41F4700                                        PUSH update.00471FE4
00471D9E   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
00471DA1   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00471DA4   . A0 BC214700                                        MOV AL,BYTE PTR DS:[4721BC]
00471DA9   . 50                                                 PUSH EAX
00471DAA   . 8D45 9C                                            LEA EAX,DWORD PTR SS:[EBP-64]
00471DAD   . 50                                                 PUSH EAX
00471DAE   . B9 C8214700                                        MOV ECX,update.004721C8
00471DB3   . BA D4214700                                        MOV EDX,update.004721D4
00471DB8   . 8B45 F4                                            MOV EAX,DWORD PTR SS:[EBP-C]
00471DBB   . E8 48BBF9FF                                        CALL update.0040D908
00471DC0   . 8B55 9C                                            MOV EDX,DWORD PTR SS:[EBP-64]
00471DC3   . 8D45 F4                                            LEA EAX,DWORD PTR SS:[EBP-C]
00471DC6   . E8 7528F9FF                                        CALL update.00404640
00471DCB   . 33C0                                               XOR EAX,EAX
00471DCD   . 55                                                 PUSH EBP
00471DCE   . 68 5A1F4700                                        PUSH update.00471F5A
00471DD3   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
00471DD6   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00471DD9   . 68 E0214700                                        PUSH update.004721E0                          ;  ASCII "http://patch.linkrealms.com/patch/"
00471DDE   . FF75 F4                                            PUSH DWORD PTR SS:[EBP-C]
00471DE1   . 68 0C224700                                        PUSH update.0047220C                          ;  ASCII ".exe"
00471DE6   . 8D45 98                                            LEA EAX,DWORD PTR SS:[EBP-68]
00471DE9   . BA 03000000                                        MOV EDX,3
00471DEE   . E8 352BF9FF                                        CALL update.00404928
00471DF3   . 8B55 98                                            MOV EDX,DWORD PTR SS:[EBP-68]
00471DF6   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471DF9   . 8B80 18030000                                      MOV EAX,DWORD PTR DS:[EAX+318]
00471DFF   . 8B4D E4                                            MOV ECX,DWORD PTR SS:[EBP-1C]
00471E02   . E8 8DC5FFFF                                        CALL update.0046E394
00471E07   . 8D55 90                                            LEA EDX,DWORD PTR SS:[EBP-70]
00471E0A   . 33C0                                               XOR EAX,EAX
00471E0C   . E8 330CF9FF                                        CALL update.00402A44
00471E11   . 8B45 90                                            MOV EAX,DWORD PTR SS:[EBP-70]
00471E14   . 8D55 94                                            LEA EDX,DWORD PTR SS:[EBP-6C]
00471E17   . E8 8871F9FF                                        CALL update.00408FA4
00471E1C   . 8D45 94                                            LEA EAX,DWORD PTR SS:[EBP-6C]
00471E1F   . BA 1C224700                                        MOV EDX,update.0047221C                       ;  ASCII "patch.exe"
00471E24   . E8 472AF9FF                                        CALL update.00404870
00471E29   . 8B55 94                                            MOV EDX,DWORD PTR SS:[EBP-6C]
00471E2C   . 8B45 E4                                            MOV EAX,DWORD PTR SS:[EBP-1C]
00471E2F   . E8 4C62FAFF                                        CALL update.00418080
00471E34   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471E37   . 05 40030000                                        ADD EAX,340
00471E3C   . 33C9                                               XOR ECX,ECX
00471E3E   . BA 10000000                                        MOV EDX,10
00471E43   . E8 CC11F9FF                                        CALL update.00403014
00471E48   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471E4B   . 05 50030000                                        ADD EAX,350
00471E50   . 33C9                                               XOR ECX,ECX
00471E52   . BA 44000000                                        MOV EDX,44
00471E57   . E8 B811F9FF                                        CALL update.00403014
00471E5C   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471E5F   . C780 50030000 44000000                             MOV DWORD PTR DS:[EAX+350],44
00471E69   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471E6C   . 05 40030000                                        ADD EAX,340
00471E71   . 50                                                 PUSH EAX
00471E72   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471E75   . 05 50030000                                        ADD EAX,350
00471E7A   . 50                                                 PUSH EAX
00471E7B   . 6A 00                                              PUSH 0
00471E7D   . 6A 00                                              PUSH 0
00471E7F   . 68 20000004                                        PUSH 4000020
00471E84   . 6A 00                                              PUSH 0
00471E86   . 6A 00                                              PUSH 0
00471E88   . 6A 00                                              PUSH 0
00471E8A   . 8D55 88                                            LEA EDX,DWORD PTR SS:[EBP-78]
00471E8D   . 33C0                                               XOR EAX,EAX
00471E8F   . E8 B00BF9FF                                        CALL update.00402A44
00471E94   . 8B45 88                                            MOV EAX,DWORD PTR SS:[EBP-78]
00471E97   . 8D55 8C                                            LEA EDX,DWORD PTR SS:[EBP-74]
00471E9A   . E8 0571F9FF                                        CALL update.00408FA4
00471E9F   . 8D45 8C                                            LEA EAX,DWORD PTR SS:[EBP-74]
00471EA2   . BA 1C224700                                        MOV EDX,update.0047221C                       ;  ASCII "patch.exe"
00471EA7   . E8 C429F9FF                                        CALL update.00404870
00471EAC   . 8B45 8C                                            MOV EAX,DWORD PTR SS:[EBP-74]
00471EAF   . E8 B42BF9FF                                        CALL update.00404A68
00471EB4   . 50                                                 PUSH EAX                                      ; |CommandLine
00471EB5   . 6A 00                                              PUSH 0                                        ; |ModuleFileName = NULL
00471EB7   . E8 644AF9FF                                        CALL <JMP.&kernel32.CreateProcessA>           ; \CreateProcessA
00471EBC   . 85C0                                               TEST EAX,EAX
00471EBE   . 74 35                                              JE SHORT update.00471EF5
00471EC0   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471EC3   . 8B80 08030000                                      MOV EAX,DWORD PTR DS:[EAX+308]
00471EC9   . BA 30224700                                        MOV EDX,update.00472230                       ;  ASCII "Applying patch..."
00471ECE   . E8 310CFCFF                                        CALL update.00432B04
00471ED3   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471ED6   . 8B80 04030000                                      MOV EAX,DWORD PTR DS:[EAX+304]
00471EDC   . 33D2                                               XOR EDX,EDX
00471EDE   . 8B08                                               MOV ECX,DWORD PTR DS:[EAX]
00471EE0   . FF51 64                                            CALL DWORD PTR DS:[ECX+64]
00471EE3   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471EE6   . 8B80 20030000                                      MOV EAX,DWORD PTR DS:[EAX+320]
00471EEC   . B2 01                                              MOV DL,1
00471EEE   . E8 F17AFBFF                                        CALL update.004299E4
00471EF3   . EB 5B                                              JMP SHORT update.00471F50
00471EF5   > 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471EF8   . 8B80 40030000                                      MOV EAX,DWORD PTR DS:[EAX+340]
00471EFE   . 50                                                 PUSH EAX                                      ; /hObject
00471EFF   . E8 F449F9FF                                        CALL <JMP.&kernel32.CloseHandle>              ; \CloseHandle
00471F04   . 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00471F06   . 66:8B0D 74204700                                   MOV CX,WORD PTR DS:[472074]                   ; |
00471F0D   . 33D2                                               XOR EDX,EDX                                   ; |
00471F0F   . B8 4C224700                                        MOV EAX,update.0047224C                       ; |ASCII "Could not execute the patch.  Your game client may be out of date and not function properly."
00471F14   . E8 5727FEFF                                        CALL update.00454670                          ; \update.00454670
00471F19   . 8D55 80                                            LEA EDX,DWORD PTR SS:[EBP-80]
00471F1C   . 33C0                                               XOR EAX,EAX
00471F1E   . E8 210BF9FF                                        CALL update.00402A44
00471F23   . 8B45 80                                            MOV EAX,DWORD PTR SS:[EBP-80]
00471F26   . 8D55 84                                            LEA EDX,DWORD PTR SS:[EBP-7C]
00471F29   . E8 7670F9FF                                        CALL update.00408FA4
00471F2E   . 8D45 84                                            LEA EAX,DWORD PTR SS:[EBP-7C]
00471F31   . BA 1C224700                                        MOV EDX,update.0047221C                       ;  ASCII "patch.exe"
00471F36   . E8 3529F9FF                                        CALL update.00404870
00471F3B   . 8B45 84                                            MOV EAX,DWORD PTR SS:[EBP-7C]
00471F3E   . E8 C96FF9FF                                        CALL update.00408F0C
00471F43   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471F46   . E8 EDF6FFFF                                        CALL update.00471638
00471F4B   . E8 E424F9FF                                        CALL update.00404434
00471F50   > 33C0                                               XOR EAX,EAX
00471F52   . 5A                                                 POP EDX
00471F53   . 59                                                 POP ECX
00471F54   . 59                                                 POP ECX
00471F55   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00471F58   . EB 74                                              JMP SHORT update.00471FCE
00471F5A   .^E9 411EF9FF                                        JMP update.00403DA0
00471F5F     01                                                 DB 01
00471F60     00                                                 DB 00
00471F61     00                                                 DB 00
00471F62     00                                                 DB 00
00471F63   . B0784000                                           DD update.004078B0
00471F67   . 6B1F4700                                           DD update.00471F6B
00471F6B   . 8945 D4                                            MOV DWORD PTR SS:[EBP-2C],EAX
00471F6E   . 8D95 78FFFFFF                                      LEA EDX,DWORD PTR SS:[EBP-88]
00471F74   . 33C0                                               XOR EAX,EAX
00471F76   . E8 C90AF9FF                                        CALL update.00402A44
00471F7B   . 8B85 78FFFFFF                                      MOV EAX,DWORD PTR SS:[EBP-88]
00471F81   . 8D95 7CFFFFFF                                      LEA EDX,DWORD PTR SS:[EBP-84]
00471F87   . E8 1870F9FF                                        CALL update.00408FA4
00471F8C   . 8D85 7CFFFFFF                                      LEA EAX,DWORD PTR SS:[EBP-84]
00471F92   . BA 1C224700                                        MOV EDX,update.0047221C                       ;  ASCII "patch.exe"
00471F97   . E8 D428F9FF                                        CALL update.00404870
00471F9C   . 8B85 7CFFFFFF                                      MOV EAX,DWORD PTR SS:[EBP-84]
00471FA2   . E8 656FF9FF                                        CALL update.00408F0C
00471FA7   . 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00471FA9   . 66:8B0D 74204700                                   MOV CX,WORD PTR DS:[472074]                   ; |
00471FB0   . 33D2                                               XOR EDX,EDX                                   ; |
00471FB2   . B8 B4224700                                        MOV EAX,update.004722B4                       ; |ASCII "Could not retrieve patch.
The patch server may be temporarily unavailable, try again later."
00471FB7   . E8 B426FEFF                                        CALL update.00454670                          ; \update.00454670
00471FBC   . 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471FBF   . E8 74F6FFFF                                        CALL update.00471638
00471FC4   . E8 6B24F9FF                                        CALL update.00404434
00471FC9   . E8 0E20F9FF                                        CALL update.00403FDC
00471FCE   > 33C0                                               XOR EAX,EAX
00471FD0   . 5A                                                 POP EDX
00471FD1   . 59                                                 POP ECX
00471FD2   . 59                                                 POP ECX
00471FD3   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00471FD6   . 68 F81F4700                                        PUSH update.00471FF8
00471FDB   > 8B45 E4                                            MOV EAX,DWORD PTR SS:[EBP-1C]
00471FDE   . E8 F117F9FF                                        CALL update.004037D4
00471FE3   . C3                                                 RETN
00471FE4   .^E9 3F1FF9FF                                        JMP update.00403F28
00471FE9   .^EB F0                                              JMP SHORT update.00471FDB
00471FEB   > 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00471FEE   . E8 45F6FFFF                                        CALL update.00471638
00471FF3   . E8 3C24F9FF                                        CALL update.00404434
00471FF8   > 33C0                                               XOR EAX,EAX
00471FFA   . 5A                                                 POP EDX
00471FFB   . 59                                                 POP ECX
00471FFC   . 59                                                 POP ECX
00471FFD   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00472000   . 68 38204700                                        PUSH update.00472038
00472005   > 8D85 78FFFFFF                                      LEA EAX,DWORD PTR SS:[EBP-88]
0047200B   . BA 16000000                                        MOV EDX,16
00472010   . E8 B725F9FF                                        CALL update.004045CC
00472015   . 8D45 F0                                            LEA EAX,DWORD PTR SS:[EBP-10]
00472018   . 8B15 90144700                                      MOV EDX,DWORD PTR DS:[471490]                 ;  update.00471494
0047201E   . E8 C938F9FF                                        CALL update.004058EC
00472023   . 8D45 F4                                            LEA EAX,DWORD PTR SS:[EBP-C]
00472026   . BA 02000000                                        MOV EDX,2
0047202B   . E8 9C25F9FF                                        CALL update.004045CC
00472030   . C3                                                 RETN
00472031   .^E9 F21EF9FF                                        JMP update.00403F28
00472036   .^EB CD                                              JMP SHORT update.00472005
00472038   . 5F                                                 POP EDI
00472039   . 5E                                                 POP ESI
0047203A   . 5B                                                 POP EBX
0047203B   . 8BE5                                               MOV ESP,EBP
0047203D   . 5D                                                 POP EBP
0047203E   . C3                                                 RETN
0047203F     00                                                 DB 00
00472040   . FFFFFFFF                                           DD FFFFFFFF
00472044   . 2B000000                                           DD 0000002B
00472048   . 68 74 74 70 3A 2F 2F 70 61 74 63 68 2E 6C 69 6E    ASCII "http://patch.lin"
00472058   . 6B 72 65 61 6C 6D 73 2E 63 6F 6D 2F 70 61 74 63    ASCII "krealms.com/patc"
00472068   . 68 2F 70 61 74 63 68 2E 74 78 74 00                ASCII "h/patch.txt",0
00472074   . 0400                                               DW 0004
00472076     00                                                 DB 00
00472077     00                                                 DB 00
00472078   . FFFFFFFF                                           DD FFFFFFFF
0047207C   . 50000000                                           DD 00000050
00472080   . 50 61 74 63 68 20 63 61 6E 63 65 6C 6C 65 64 2E    ASCII "Patch cancelled."
00472090   . 20 20 59 6F 75 72 20 67 61 6D 65 20 63 6C 69 65    ASCII "  Your game clie"
004720A0   . 6E 74 20 6D 61 79 20 62 65 20 6F 75 74 20 6F 66    ASCII "nt may be out of"
004720B0   . 20 64 61 74 65 20 61 6E 64 20 6E 6F 74 20 66 75    ASCII " date and not fu"
004720C0   . 6E 63 74 69 6F 6E 20 70 72 6F 70 65 72 6C 79 2E    ASCII "nction properly."
004720D0   . 00                                                 ASCII 0
004720D1     00                                                 DB 00
004720D2     00                                                 DB 00
004720D3     00                                                 DB 00
004720D4   . FFFFFFFF                                           DD FFFFFFFF
004720D8   . 0E000000                                           DD 0000000E
004720DC   . 6C 69 6E 6B 72 65 61 6C 6D 73 2E 65 78 65 00       ASCII "linkrealms.exe",0
004720EB     00                                                 DB 00
004720EC   . 6F 70 65 6E 00                                     ASCII "open",0
004720F1     00                                                 DB 00
004720F2     00                                                 DB 00
004720F3     00                                                 DB 00
004720F4   . FFFFFFFF                                           DD FFFFFFFF
004720F8   . 0A000000                                           DD 0000000A
004720FC   . 45 6D 70 74 79 20 4C 69 73 74 00                   ASCII "Empty List",0
00472107     00                                                 DB 00
00472108   . FFFFFFFF                                           DD FFFFFFFF
0047210C   . 56000000                                           DD 00000056
00472110   . 43 6F 75 6C 64 20 6E 6F 74 20 72 65 74 72 69 65    ASCII "Could not retrie"
00472120   . 76 65 20 70 61 74 63 68 20 69 6E 66 6F 72 6D 61    ASCII "ve patch informa"
00472130   . 74 69 6F 6E 2E 0D 54 68 65 20 70 61 74 63 68 20    ASCII "tion.
The patch "
00472140   . 73 65 72 76 65 72 20 6D 61 79 20 62 65 20 74 65    ASCII "server may be te"
00472150   . 6D 70 6F 72 61 72 69 6C 79 20 75 6E 61 76 61 69    ASCII "mporarily unavai"
00472160   . 6C 61 62 6C 65 2E 00                               ASCII "lable.",0
00472167     00                                                 DB 00
00472168   . FFFFFFFF                                           DD FFFFFFFF
0047216C   . 10000000                                           DD 00000010
00472170   . 70 61 74 63 68 5F 75 70 64 61 74 65 2E 65 78 65    ASCII "patch_update.exe"
00472180   . 00                                                 ASCII 0
00472181     00                                                 DB 00
00472182     00                                                 DB 00
00472183     00                                                 DB 00
00472184   . FFFFFFFF                                           DD FFFFFFFF
00472188   . 12000000                                           DD 00000012
0047218C   . 44 6F 77 6E 6C 6F 61 64 69 6E 67 20 70 61 74 63    ASCII "Downloading patc"
0047219C   . 68 20 00                                           ASCII "h ",0
0047219F     00                                                 DB 00
004721A0   . FFFFFFFF                                           DD FFFFFFFF
004721A4   . 04000000                                           DD 00000004
004721A8   . 20 6F 66 20 00                                     ASCII " of ",0
004721AD     00                                                 DB 00
004721AE     00                                                 DB 00
004721AF     00                                                 DB 00
004721B0   . FFFFFFFF                                           DD FFFFFFFF
004721B4   . 03000000                                           DD 00000003
004721B8   . 2E 2E 2E 00                                        ASCII "...",0
004721BC   . 01                                                 DB 01
004721BD     00                                                 DB 00
004721BE     00                                                 DB 00
004721BF     00                                                 DB 00
004721C0   . FFFFFFFF                                           DD FFFFFFFF
004721C4   . 01000000                                           DD 00000001
004721C8   . 5F 00                                              ASCII "_",0
004721CA     00                                                 DB 00
004721CB     00                                                 DB 00
004721CC   . FFFFFFFF                                           DD FFFFFFFF
004721D0   . 01000000                                           DD 00000001
004721D4   . 2E 00                                              ASCII ".",0
004721D6     00                                                 DB 00
004721D7     00                                                 DB 00
004721D8   . FFFFFFFF                                           DD FFFFFFFF
004721DC   . 22000000                                           DD 00000022
004721E0   . 68 74 74 70 3A 2F 2F 70 61 74 63 68 2E 6C 69 6E    ASCII "http://patch.lin"
004721F0   . 6B 72 65 61 6C 6D 73 2E 63 6F 6D 2F 70 61 74 63    ASCII "krealms.com/patc"
00472200   . 68 2F 00                                           ASCII "h/",0
00472203     00                                                 DB 00
00472204   . FFFFFFFF                                           DD FFFFFFFF
00472208   . 04000000                                           DD 00000004
0047220C   . 2E 65 78 65 00                                     ASCII ".exe",0
00472211     00                                                 DB 00
00472212     00                                                 DB 00
00472213     00                                                 DB 00
00472214   . FFFFFFFF                                           DD FFFFFFFF
00472218   . 09000000                                           DD 00000009
0047221C   . 70 61 74 63 68 2E 65 78 65 00                      ASCII "patch.exe",0
00472226     00                                                 DB 00
00472227     00                                                 DB 00
00472228   . FFFFFFFF                                           DD FFFFFFFF
0047222C   . 11000000                                           DD 00000011
00472230   . 41 70 70 6C 79 69 6E 67 20 70 61 74 63 68 2E 2E    ASCII "Applying patch.."
00472240   . 2E 00                                              ASCII ".",0
00472242     00                                                 DB 00
00472243     00                                                 DB 00
00472244   . FFFFFFFF                                           DD FFFFFFFF
00472248   . 5C000000                                           DD 0000005C
0047224C   . 43 6F 75 6C 64 20 6E 6F 74 20 65 78 65 63 75 74    ASCII "Could not execut"
0047225C   . 65 20 74 68 65 20 70 61 74 63 68 2E 20 20 59 6F    ASCII "e the patch.  Yo"
0047226C   . 75 72 20 67 61 6D 65 20 63 6C 69 65 6E 74 20 6D    ASCII "ur game client m"
0047227C   . 61 79 20 62 65 20 6F 75 74 20 6F 66 20 64 61 74    ASCII "ay be out of dat"
0047228C   . 65 20 61 6E 64 20 6E 6F 74 20 66 75 6E 63 74 69    ASCII "e and not functi"
0047229C   . 6F 6E 20 70 72 6F 70 65 72 6C 79 2E 00             ASCII "on properly.",0
004722A9     00                                                 DB 00
004722AA     00                                                 DB 00
004722AB     00                                                 DB 00
004722AC   . FFFFFFFF                                           DD FFFFFFFF
004722B0   . 5B000000                                           DD 0000005B
004722B4   . 43 6F 75 6C 64 20 6E 6F 74 20 72 65 74 72 69 65    ASCII "Could not retrie"
004722C4   . 76 65 20 70 61 74 63 68 2E 0D 54 68 65 20 70 61    ASCII "ve patch.
The pa"
004722D4   . 74 63 68 20 73 65 72 76 65 72 20 6D 61 79 20 62    ASCII "tch server may b"
004722E4   . 65 20 74 65 6D 70 6F 72 61 72 69 6C 79 20 75 6E    ASCII "e temporarily un"
004722F4   . 61 76 61 69 6C 61 62 6C 65 2C 20 74 72 79 20 61    ASCII "available, try a"
00472304   . 67 61 69 6E 20 6C 61 74 65 72 2E 00                ASCII "gain later.",0
00472310  /$ 55                                                 PUSH EBP
00472311  |. 8BEC                                               MOV EBP,ESP
00472313  |. 83C4 CC                                            ADD ESP,-34
00472316  |. 894D F4                                            MOV DWORD PTR SS:[EBP-C],ECX
00472319  |. 8955 F8                                            MOV DWORD PTR SS:[EBP-8],EDX
0047231C  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
0047231F  |. C645 F3 01                                         MOV BYTE PTR SS:[EBP-D],1
00472323  |. 33C0                                               XOR EAX,EAX
00472325  |. 8A45 F3                                            MOV AL,BYTE PTR SS:[EBP-D]
00472328  |. C1E0 0A                                            SHL EAX,0A
0047232B  |. 66:8945 F0                                         MOV WORD PTR SS:[EBP-10],AX
0047232F  |. 0FB745 F0                                          MOVZX EAX,WORD PTR SS:[EBP-10]
00472333  |. 69C0 E8030000                                      IMUL EAX,EAX,3E8
00472339  |. 8945 EC                                            MOV DWORD PTR SS:[EBP-14],EAX
0047233C  |. 6945 EC E8030000                                   IMUL EAX,DWORD PTR SS:[EBP-14],3E8
00472343  |. 8945 E8                                            MOV DWORD PTR SS:[EBP-18],EAX
00472346  |. 6945 E8 E8030000                                   IMUL EAX,DWORD PTR SS:[EBP-18],3E8
0047234D  |. 33D2                                               XOR EDX,EDX
0047234F  |. 8945 E0                                            MOV DWORD PTR SS:[EBP-20],EAX
00472352  |. 8955 E4                                            MOV DWORD PTR SS:[EBP-1C],EDX
00472355  |. 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
00472358  |. 33D2                                               XOR EDX,EDX
0047235A  |. 3B55 E4                                            CMP EDX,DWORD PTR SS:[EBP-1C]
0047235D  |. 75 07                                              JNZ SHORT update.00472366
0047235F  |. 3B45 E0                                            CMP EAX,DWORD PTR SS:[EBP-20]
00472362  |. 76 48                                              JBE SHORT update.004723AC
00472364  |. EB 02                                              JMP SHORT update.00472368
00472366  |> 7E 44                                              JLE SHORT update.004723AC
00472368  |> 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
0047236B  |. 8945 D8                                            MOV DWORD PTR SS:[EBP-28],EAX
0047236E  |. 33C0                                               XOR EAX,EAX
00472370  |. 8945 DC                                            MOV DWORD PTR SS:[EBP-24],EAX
00472373  |. DF6D D8                                            FILD QWORD PTR SS:[EBP-28]
00472376  |. 8B45 E0                                            MOV EAX,DWORD PTR SS:[EBP-20]
00472379  |. 8B55 E4                                            MOV EDX,DWORD PTR SS:[EBP-1C]
0047237C  |. 8945 D0                                            MOV DWORD PTR SS:[EBP-30],EAX
0047237F  |. 81EA 00000080                                      SUB EDX,80000000
00472385  |. 8955 D4                                            MOV DWORD PTR SS:[EBP-2C],EDX
00472388  |. DF6D D0                                            FILD QWORD PTR SS:[EBP-30]
0047238B  |. DC05 88244700                                      FADD QWORD PTR DS:[472488]
00472391  |. DEF9                                               FDIVP ST(1),ST
00472393  |. 83C4 F4                                            ADD ESP,-0C
00472396  |. DB3C24                                             FSTP TBYTE PTR SS:[ESP]                       ; |
00472399  |. 9B                                                 WAIT                                          ; |
0047239A  |. 8B55 F4                                            MOV EDX,DWORD PTR SS:[EBP-C]                  ; |
0047239D  |. B8 9C244700                                        MOV EAX,update.0047249C                       ; |ASCII "#.## TB"
004723A2  |. E8 BD7EF9FF                                        CALL update.0040A264                          ; \update.0040A264
004723A7  |. E9 D6000000                                        JMP update.00472482
004723AC  |> 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
004723AF  |. 3B45 E8                                            CMP EAX,DWORD PTR SS:[EBP-18]
004723B2  |. 76 37                                              JBE SHORT update.004723EB
004723B4  |. 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
004723B7  |. 8945 D8                                            MOV DWORD PTR SS:[EBP-28],EAX
004723BA  |. 33C0                                               XOR EAX,EAX
004723BC  |. 8945 DC                                            MOV DWORD PTR SS:[EBP-24],EAX
004723BF  |. DF6D D8                                            FILD QWORD PTR SS:[EBP-28]
004723C2  |. 8B45 E8                                            MOV EAX,DWORD PTR SS:[EBP-18]
004723C5  |. 8945 D0                                            MOV DWORD PTR SS:[EBP-30],EAX
004723C8  |. 33C0                                               XOR EAX,EAX
004723CA  |. 8945 D4                                            MOV DWORD PTR SS:[EBP-2C],EAX
004723CD  |. DF6D D0                                            FILD QWORD PTR SS:[EBP-30]
004723D0  |. DEF9                                               FDIVP ST(1),ST
004723D2  |. 83C4 F4                                            ADD ESP,-0C
004723D5  |. DB3C24                                             FSTP TBYTE PTR SS:[ESP]                       ; |
004723D8  |. 9B                                                 WAIT                                          ; |
004723D9  |. 8B55 F4                                            MOV EDX,DWORD PTR SS:[EBP-C]                  ; |
004723DC  |. B8 AC244700                                        MOV EAX,update.004724AC                       ; |ASCII "#.## GB"
004723E1  |. E8 7E7EF9FF                                        CALL update.0040A264                          ; \update.0040A264
004723E6  |. E9 97000000                                        JMP update.00472482
004723EB  |> 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
004723EE  |. 3B45 EC                                            CMP EAX,DWORD PTR SS:[EBP-14]
004723F1  |. 76 34                                              JBE SHORT update.00472427
004723F3  |. 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
004723F6  |. 8945 D8                                            MOV DWORD PTR SS:[EBP-28],EAX
004723F9  |. 33C0                                               XOR EAX,EAX
004723FB  |. 8945 DC                                            MOV DWORD PTR SS:[EBP-24],EAX
004723FE  |. DF6D D8                                            FILD QWORD PTR SS:[EBP-28]
00472401  |. 8B45 EC                                            MOV EAX,DWORD PTR SS:[EBP-14]
00472404  |. 8945 D0                                            MOV DWORD PTR SS:[EBP-30],EAX
00472407  |. 33C0                                               XOR EAX,EAX
00472409  |. 8945 D4                                            MOV DWORD PTR SS:[EBP-2C],EAX
0047240C  |. DF6D D0                                            FILD QWORD PTR SS:[EBP-30]
0047240F  |. DEF9                                               FDIVP ST(1),ST
00472411  |. 83C4 F4                                            ADD ESP,-0C
00472414  |. DB3C24                                             FSTP TBYTE PTR SS:[ESP]                       ; |
00472417  |. 9B                                                 WAIT                                          ; |
00472418  |. 8B55 F4                                            MOV EDX,DWORD PTR SS:[EBP-C]                  ; |
0047241B  |. B8 BC244700                                        MOV EAX,update.004724BC                       ; |ASCII "#.## MB"
00472420  |. E8 3F7EF9FF                                        CALL update.0040A264                          ; \update.0040A264
00472425  |. EB 5B                                              JMP SHORT update.00472482
00472427  |> 0FB745 F0                                          MOVZX EAX,WORD PTR SS:[EBP-10]
0047242B  |. 3B45 F8                                            CMP EAX,DWORD PTR SS:[EBP-8]
0047242E  |. 73 30                                              JNB SHORT update.00472460
00472430  |. 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
00472433  |. 8945 D8                                            MOV DWORD PTR SS:[EBP-28],EAX
00472436  |. 33C0                                               XOR EAX,EAX
00472438  |. 8945 DC                                            MOV DWORD PTR SS:[EBP-24],EAX
0047243B  |. DF6D D8                                            FILD QWORD PTR SS:[EBP-28]
0047243E  |. 0FB745 F0                                          MOVZX EAX,WORD PTR SS:[EBP-10]
00472442  |. 8945 CC                                            MOV DWORD PTR SS:[EBP-34],EAX
00472445  |. DB45 CC                                            FILD DWORD PTR SS:[EBP-34]
00472448  |. DEF9                                               FDIVP ST(1),ST
0047244A  |. 83C4 F4                                            ADD ESP,-0C
0047244D  |. DB3C24                                             FSTP TBYTE PTR SS:[ESP]                       ; |
00472450  |. 9B                                                 WAIT                                          ; |
00472451  |. 8B55 F4                                            MOV EDX,DWORD PTR SS:[EBP-C]                  ; |
00472454  |. B8 CC244700                                        MOV EAX,update.004724CC                       ; |ASCII "#.## KB"
00472459  |. E8 067EF9FF                                        CALL update.0040A264                          ; \update.0040A264
0047245E  |. EB 22                                              JMP SHORT update.00472482
00472460  |> 8B45 F8                                            MOV EAX,DWORD PTR SS:[EBP-8]
00472463  |. 8945 D8                                            MOV DWORD PTR SS:[EBP-28],EAX
00472466  |. 33C0                                               XOR EAX,EAX
00472468  |. 8945 DC                                            MOV DWORD PTR SS:[EBP-24],EAX
0047246B  |. DF6D D8                                            FILD QWORD PTR SS:[EBP-28]
0047246E  |. 83C4 F4                                            ADD ESP,-0C
00472471  |. DB3C24                                             FSTP TBYTE PTR SS:[ESP]                       ; |
00472474  |. 9B                                                 WAIT                                          ; |
00472475  |. 8B55 F4                                            MOV EDX,DWORD PTR SS:[EBP-C]                  ; |
00472478  |. B8 DC244700                                        MOV EAX,update.004724DC                       ; |ASCII "#.## bytes"
0047247D  |. E8 E27DF9FF                                        CALL update.0040A264                          ; \update.0040A264
00472482  |> 8BE5                                               MOV ESP,EBP
00472484  |. 5D                                                 POP EBP
00472485  \. C3                                                 RETN
00472486     00                                                 DB 00
00472487     00                                                 DB 00
00472488   . 0000000000000080                                   DQ FLOAT 0.0
00472490   . 3E 40 00                                           ASCII ">@",0
00472493     00                                                 DB 00
00472494   . FFFFFFFF                                           DD FFFFFFFF
00472498   . 07000000                                           DD 00000007
0047249C   . 23 2E 23 23 20 54 42 00                            ASCII "#.## TB",0
004724A4   . FFFFFFFF                                           DD FFFFFFFF
004724A8   . 07000000                                           DD 00000007
004724AC   . 23 2E 23 23 20 47 42 00                            ASCII "#.## GB",0
004724B4   . FFFFFFFF                                           DD FFFFFFFF
004724B8   . 07000000                                           DD 00000007
004724BC   . 23 2E 23 23 20 4D 42 00                            ASCII "#.## MB",0
004724C4   . FFFFFFFF                                           DD FFFFFFFF
004724C8   . 07000000                                           DD 00000007
004724CC   . 23 2E 23 23 20 4B 42 00                            ASCII "#.## KB",0
004724D4   . FFFFFFFF                                           DD FFFFFFFF
004724D8   . 0A000000                                           DD 0000000A
004724DC   . 23 2E 23 23 20 62 79 74 65 73 00                   ASCII "#.## bytes",0
004724E7     00                                                 DB 00
004724E8  /. 55                                                 PUSH EBP
004724E9  |. 8BEC                                               MOV EBP,ESP
004724EB  |. 83C4 F8                                            ADD ESP,-8
004724EE  |. 8955 F8                                            MOV DWORD PTR SS:[EBP-8],EDX
004724F1  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
004724F4  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004724F7  |. 33D2                                               XOR EDX,EDX
004724F9  |. 8990 28030000                                      MOV DWORD PTR DS:[EAX+328],EDX
004724FF  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472502  |. C680 30030000 01                                   MOV BYTE PTR DS:[EAX+330],1
00472509  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047250C  |. C680 3C030000 00                                   MOV BYTE PTR DS:[EAX+33C],0
00472513  |. B2 01                                              MOV DL,1
00472515  |. A1 AC314100                                        MOV EAX,DWORD PTR DS:[4131AC]
0047251A  |. E8 8512F9FF                                        CALL update.004037A4
0047251F  |. 8B55 FC                                            MOV EDX,DWORD PTR SS:[EBP-4]
00472522  |. 8982 34030000                                      MOV DWORD PTR DS:[EDX+334],EAX
00472528  |. 59                                                 POP ECX
00472529  |. 59                                                 POP ECX
0047252A  |. 5D                                                 POP EBP
0047252B  \. C3                                                 RETN
0047252C  /. 55                                                 PUSH EBP
0047252D  |. 8BEC                                               MOV EBP,ESP
0047252F  |. 83C4 F8                                            ADD ESP,-8
00472532  |. 8955 F8                                            MOV DWORD PTR SS:[EBP-8],EDX
00472535  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
00472538  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047253B  |. 83B8 34030000 00                                   CMP DWORD PTR DS:[EAX+334],0
00472542  |. 74 0E                                              JE SHORT update.00472552
00472544  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472547  |. 8B80 34030000                                      MOV EAX,DWORD PTR DS:[EAX+334]
0047254D  |. E8 8212F9FF                                        CALL update.004037D4
00472552  |> 59                                                 POP ECX
00472553  |. 59                                                 POP ECX
00472554  |. 5D                                                 POP EBP
00472555  \. C3                                                 RETN
00472556     8BC0                                               MOV EAX,EAX
00472558  /. 55                                                 PUSH EBP
00472559  |. 8BEC                                               MOV EBP,ESP
0047255B  |. 83C4 E8                                            ADD ESP,-18
0047255E  |. 53                                                 PUSH EBX
0047255F  |. 33DB                                               XOR EBX,EBX
00472561  |. 895D F0                                            MOV DWORD PTR SS:[EBP-10],EBX
00472564  |. 895D EC                                            MOV DWORD PTR SS:[EBP-14],EBX
00472567  |. 895D E8                                            MOV DWORD PTR SS:[EBP-18],EBX
0047256A  |. 884D F7                                            MOV BYTE PTR SS:[EBP-9],CL
0047256D  |. 8955 F8                                            MOV DWORD PTR SS:[EBP-8],EDX
00472570  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
00472573  |. 33C0                                               XOR EAX,EAX
00472575  |. 55                                                 PUSH EBP
00472576  |. 68 39264700                                        PUSH update.00472639
0047257B  |. 64:FF30                                            PUSH DWORD PTR FS:[EAX]
0047257E  |. 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00472581  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472584  |. 80B8 3C030000 00                                   CMP BYTE PTR DS:[EAX+33C],0
0047258B  |. 74 22                                              JE SHORT update.004725AF
0047258D  |. 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
0047258F  |. 66:8B0D 48264700                                   MOV CX,WORD PTR DS:[472648]                   ; |
00472596  |. 33D2                                               XOR EDX,EDX                                   ; |
00472598  |. B8 54264700                                        MOV EAX,update.00472654                       ; |ASCII "Patch cancelled.  Your game client may be out of date and not function properly."
0047259D  |. E8 CE20FEFF                                        CALL update.00454670                          ; \update.00454670
004725A2  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004725A5  |. E8 8EF0FFFF                                        CALL update.00471638
004725AA  |. E8 851EF9FF                                        CALL update.00404434
004725AF  |> 8B55 08                                            MOV EDX,DWORD PTR SS:[EBP+8]
004725B2  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004725B5  |. 8B80 00030000                                      MOV EAX,DWORD PTR DS:[EAX+300]
004725BB  |. E8 8833FEFF                                        CALL update.00455948
004725C0  |. 8D4D EC                                            LEA ECX,DWORD PTR SS:[EBP-14]
004725C3  |. 8B55 08                                            MOV EDX,DWORD PTR SS:[EBP+8]
004725C6  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004725C9  |. E8 42FDFFFF                                        CALL update.00472310
004725CE  |. FF75 EC                                            PUSH DWORD PTR SS:[EBP-14]
004725D1  |. 68 B0264700                                        PUSH update.004726B0                          ;  ASCII " of "
004725D6  |. 8D4D E8                                            LEA ECX,DWORD PTR SS:[EBP-18]
004725D9  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004725DC  |. 8B90 38030000                                      MOV EDX,DWORD PTR DS:[EAX+338]
004725E2  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004725E5  |. E8 26FDFFFF                                        CALL update.00472310
004725EA  |. FF75 E8                                            PUSH DWORD PTR SS:[EBP-18]
004725ED  |. 8D45 F0                                            LEA EAX,DWORD PTR SS:[EBP-10]
004725F0  |. BA 03000000                                        MOV EDX,3
004725F5  |. E8 2E23F9FF                                        CALL update.00404928
004725FA  |. 8B55 F0                                            MOV EDX,DWORD PTR SS:[EBP-10]
004725FD  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472600  |. 8B80 1C030000                                      MOV EAX,DWORD PTR DS:[EAX+31C]
00472606  |. E8 F904FCFF                                        CALL update.00432B04
0047260B  |. BA 11010000                                        MOV EDX,111
00472610  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472613  |. 8B80 1C030000                                      MOV EAX,DWORD PTR DS:[EAX+31C]
00472619  |. E8 82FCFBFF                                        CALL update.004322A0
0047261E  |. 33C0                                               XOR EAX,EAX
00472620  |. 5A                                                 POP EDX
00472621  |. 59                                                 POP ECX
00472622  |. 59                                                 POP ECX
00472623  |. 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00472626  |. 68 40264700                                        PUSH update.00472640
0047262B  |> 8D45 E8                                            LEA EAX,DWORD PTR SS:[EBP-18]
0047262E  |. BA 03000000                                        MOV EDX,3
00472633  |. E8 941FF9FF                                        CALL update.004045CC
00472638  \. C3                                                 RETN
00472639   .^E9 EA18F9FF                                        JMP update.00403F28
0047263E   .^EB EB                                              JMP SHORT update.0047262B
00472640   . 5B                                                 POP EBX
00472641   . 8BE5                                               MOV ESP,EBP
00472643   . 5D                                                 POP EBP
00472644   . C2 0400                                            RETN 4
00472647     00                                                 DB 00
00472648   . 0400                                               DW 0004
0047264A     00                                                 DB 00
0047264B     00                                                 DB 00
0047264C   . FFFFFFFF                                           DD FFFFFFFF
00472650   . 50000000                                           DD 00000050
00472654   . 50 61 74 63 68 20 63 61 6E 63 65 6C 6C 65 64 2E    ASCII "Patch cancelled."
00472664   . 20 20 59 6F 75 72 20 67 61 6D 65 20 63 6C 69 65    ASCII "  Your game clie"
00472674   . 6E 74 20 6D 61 79 20 62 65 20 6F 75 74 20 6F 66    ASCII "nt may be out of"
00472684   . 20 64 61 74 65 20 61 6E 64 20 6E 6F 74 20 66 75    ASCII " date and not fu"
00472694   . 6E 63 74 69 6F 6E 20 70 72 6F 70 65 72 6C 79 2E    ASCII "nction properly."
004726A4   . 00                                                 ASCII 0
004726A5     00                                                 DB 00
004726A6     00                                                 DB 00
004726A7     00                                                 DB 00
004726A8   . FFFFFFFF                                           DD FFFFFFFF
004726AC   . 04000000                                           DD 00000004
004726B0   . 20 6F 66 20 00                                     ASCII " of ",0
004726B5     00                                                 DB 00
004726B6     00                                                 DB 00
004726B7     00                                                 DB 00
004726B8  /. 55                                                 PUSH EBP
004726B9  |. 8BEC                                               MOV EBP,ESP
004726BB  |. 83C4 F4                                            ADD ESP,-0C
004726BE  |. 884D F7                                            MOV BYTE PTR SS:[EBP-9],CL
004726C1  |. 8955 F8                                            MOV DWORD PTR SS:[EBP-8],EDX
004726C4  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
004726C7  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004726CA  |. 80B8 3C030000 00                                   CMP BYTE PTR DS:[EAX+33C],0
004726D1  |. 74 22                                              JE SHORT update.004726F5
004726D3  |. 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
004726D5  |. 66:8B0D 18274700                                   MOV CX,WORD PTR DS:[472718]                   ; |
004726DC  |. 33D2                                               XOR EDX,EDX                                   ; |
004726DE  |. B8 24274700                                        MOV EAX,update.00472724                       ; |ASCII "Patch cancelled.  Your game client may be out of date and not function properly."
004726E3  |. E8 881FFEFF                                        CALL update.00454670                          ; \update.00454670
004726E8  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004726EB  |. E8 48EFFFFF                                        CALL update.00471638
004726F0  |. E8 3F1DF9FF                                        CALL update.00404434
004726F5  |> 8B45 08                                            MOV EAX,DWORD PTR SS:[EBP+8]
004726F8  |. 8B55 FC                                            MOV EDX,DWORD PTR SS:[EBP-4]
004726FB  |. 8982 38030000                                      MOV DWORD PTR DS:[EDX+338],EAX
00472701  |. 8B55 08                                            MOV EDX,DWORD PTR SS:[EBP+8]
00472704  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472707  |. 8B80 00030000                                      MOV EAX,DWORD PTR DS:[EAX+300]
0047270D  |. E8 8631FEFF                                        CALL update.00455898
00472712  |. 8BE5                                               MOV ESP,EBP
00472714  |. 5D                                                 POP EBP
00472715  \. C2 0400                                            RETN 4
00472718   . 0400                                               DW 0004
0047271A     00                                                 DB 00
0047271B     00                                                 DB 00
0047271C   . FFFFFFFF                                           DD FFFFFFFF
00472720   . 50000000                                           DD 00000050
00472724   . 50 61 74 63 68 20 63 61 6E 63 65 6C 6C 65 64 2E    ASCII "Patch cancelled."
00472734   . 20 20 59 6F 75 72 20 67 61 6D 65 20 63 6C 69 65    ASCII "  Your game clie"
00472744   . 6E 74 20 6D 61 79 20 62 65 20 6F 75 74 20 6F 66    ASCII "nt may be out of"
00472754   . 20 64 61 74 65 20 61 6E 64 20 6E 6F 74 20 66 75    ASCII " date and not fu"
00472764   . 6E 63 74 69 6F 6E 20 70 72 6F 70 65 72 6C 79 2E    ASCII "nction properly."
00472774   . 00                                                 ASCII 0
00472775     00                                                 DB 00
00472776     00                                                 DB 00
00472777     00                                                 DB 00
00472778  /. 55                                                 PUSH EBP
00472779  |. 8BEC                                               MOV EBP,ESP
0047277B  |. 83C4 F4                                            ADD ESP,-0C
0047277E  |. 884D F7                                            MOV BYTE PTR SS:[EBP-9],CL
00472781  |. 8955 F8                                            MOV DWORD PTR SS:[EBP-8],EDX
00472784  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
00472787  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047278A  |. 80B8 3C030000 00                                   CMP BYTE PTR DS:[EAX+33C],0
00472791  |. 74 22                                              JE SHORT update.004727B5
00472793  |. 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00472795  |. 66:8B0D E0274700                                   MOV CX,WORD PTR DS:[4727E0]                   ; |
0047279C  |. 33D2                                               XOR EDX,EDX                                   ; |
0047279E  |. B8 EC274700                                        MOV EAX,update.004727EC                       ; |ASCII "Patch cancelled.  Your game client may be out of date and not function properly."
004727A3  |. E8 C81EFEFF                                        CALL update.00454670                          ; \update.00454670
004727A8  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004727AB  |. E8 88EEFFFF                                        CALL update.00471638
004727B0  |. E8 7F1CF9FF                                        CALL update.00404434
004727B5  |> 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004727B8  |. 8B90 38030000                                      MOV EDX,DWORD PTR DS:[EAX+338]
004727BE  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004727C1  |. 8B80 00030000                                      MOV EAX,DWORD PTR DS:[EAX+300]
004727C7  |. E8 7C31FEFF                                        CALL update.00455948
004727CC  |. 33D2                                               XOR EDX,EDX
004727CE  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004727D1  |. 8B80 1C030000                                      MOV EAX,DWORD PTR DS:[EAX+31C]
004727D7  |. E8 2803FCFF                                        CALL update.00432B04
004727DC  |. 8BE5                                               MOV ESP,EBP
004727DE  |. 5D                                                 POP EBP
004727DF  \. C3                                                 RETN
004727E0   . 0400                                               DW 0004
004727E2     00                                                 DB 00
004727E3     00                                                 DB 00
004727E4   . FFFFFFFF                                           DD FFFFFFFF
004727E8   . 50000000                                           DD 00000050
004727EC   . 50 61 74 63 68 20 63 61 6E 63 65 6C 6C 65 64 2E    ASCII "Patch cancelled."
004727FC   . 20 20 59 6F 75 72 20 67 61 6D 65 20 63 6C 69 65    ASCII "  Your game clie"
0047280C   . 6E 74 20 6D 61 79 20 62 65 20 6F 75 74 20 6F 66    ASCII "nt may be out of"
0047281C   . 20 64 61 74 65 20 61 6E 64 20 6E 6F 74 20 66 75    ASCII " date and not fu"
0047282C   . 6E 63 74 69 6F 6E 20 70 72 6F 70 65 72 6C 79 2E    ASCII "nction properly."
0047283C   . 00                                                 ASCII 0
0047283D     00                                                 DB 00
0047283E     00                                                 DB 00
0047283F     00                                                 DB 00
00472840  /. 55                                                 PUSH EBP
00472841  |. 8BEC                                               MOV EBP,ESP
00472843  |. 83C4 F8                                            ADD ESP,-8
00472846  |. 8955 F8                                            MOV DWORD PTR SS:[EBP-8],EDX
00472849  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
0047284C  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047284F  |. 8B80 20030000                                      MOV EAX,DWORD PTR DS:[EAX+320]
00472855  |. 8078 40 00                                         CMP BYTE PTR DS:[EAX+40],0
00472859  |. 75 2C                                              JNZ SHORT update.00472887
0047285B  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047285E  |. C680 3C030000 01                                   MOV BYTE PTR DS:[EAX+33C],1
00472865  |. 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00472867  |. 66:8B0D 8C284700                                   MOV CX,WORD PTR DS:[47288C]                   ; |
0047286E  |. 33D2                                               XOR EDX,EDX                                   ; |
00472870  |. B8 98284700                                        MOV EAX,update.00472898                       ; |ASCII "Patch cancelled.  Your game client may be out of date and not function properly."
00472875  |. E8 F61DFEFF                                        CALL update.00454670                          ; \update.00454670
0047287A  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047287D  |. E8 B6EDFFFF                                        CALL update.00471638
00472882  |. E8 AD1BF9FF                                        CALL update.00404434
00472887  |> 59                                                 POP ECX
00472888  |. 59                                                 POP ECX
00472889  |. 5D                                                 POP EBP
0047288A  \. C3                                                 RETN
0047288B     00                                                 DB 00
0047288C   . 0400                                               DW 0004
0047288E     00                                                 DB 00
0047288F     00                                                 DB 00
00472890   . FFFFFFFF                                           DD FFFFFFFF
00472894   . 50000000                                           DD 00000050
00472898   . 50 61 74 63 68 20 63 61 6E 63 65 6C 6C 65 64 2E    ASCII "Patch cancelled."
004728A8   . 20 20 59 6F 75 72 20 67 61 6D 65 20 63 6C 69 65    ASCII "  Your game clie"
004728B8   . 6E 74 20 6D 61 79 20 62 65 20 6F 75 74 20 6F 66    ASCII "nt may be out of"
004728C8   . 20 64 61 74 65 20 61 6E 64 20 6E 6F 74 20 66 75    ASCII " date and not fu"
004728D8   . 6E 63 74 69 6F 6E 20 70 72 6F 70 65 72 6C 79 2E    ASCII "nction properly."
004728E8   . 00                                                 ASCII 0
004728E9     00                                                 DB 00
004728EA     00                                                 DB 00
004728EB     00                                                 DB 00
004728EC  /. 55                                                 PUSH EBP
004728ED  |. 8BEC                                               MOV EBP,ESP
004728EF  |. 83C4 EC                                            ADD ESP,-14
004728F2  |. 33C9                                               XOR ECX,ECX
004728F4  |. 894D F0                                            MOV DWORD PTR SS:[EBP-10],ECX
004728F7  |. 894D EC                                            MOV DWORD PTR SS:[EBP-14],ECX
004728FA  |. 8955 F4                                            MOV DWORD PTR SS:[EBP-C],EDX
004728FD  |. 8945 FC                                            MOV DWORD PTR SS:[EBP-4],EAX
00472900  |. 33C0                                               XOR EAX,EAX
00472902  |. 55                                                 PUSH EBP
00472903  |. 68 5D2A4700                                        PUSH update.00472A5D
00472908  |. 64:FF30                                            PUSH DWORD PTR FS:[EAX]
0047290B  |. 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
0047290E  |. 33D2                                               XOR EDX,EDX
00472910  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472913  |. 8B80 20030000                                      MOV EAX,DWORD PTR DS:[EAX+320]
00472919  |. E8 C670FBFF                                        CALL update.004299E4
0047291E  |. 8D45 F8                                            LEA EAX,DWORD PTR SS:[EBP-8]
00472921  |. 50                                                 PUSH EAX                                      ; /pExitCode
00472922  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]                  ; |
00472925  |. 8B80 40030000                                      MOV EAX,DWORD PTR DS:[EAX+340]                ; |
0047292B  |. 50                                                 PUSH EAX                                      ; |hProcess
0047292C  |. E8 A740F9FF                                        CALL <JMP.&kernel32.GetExitCodeProcess>       ; \GetExitCodeProcess
00472931  |. 85C0                                               TEST EAX,EAX
00472933  |. 0F84 C7000000                                      JE update.00472A00
00472939  |. 817D F8 03010000                                   CMP DWORD PTR SS:[EBP-8],103
00472940  |. 75 15                                              JNZ SHORT update.00472957
00472942  |. B2 01                                              MOV DL,1
00472944  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472947  |. 8B80 20030000                                      MOV EAX,DWORD PTR DS:[EAX+320]
0047294D  |. E8 9270FBFF                                        CALL update.004299E4
00472952  |. E9 EB000000                                        JMP update.00472A42
00472957  |> 8D55 EC                                            LEA EDX,DWORD PTR SS:[EBP-14]
0047295A  |. 33C0                                               XOR EAX,EAX
0047295C  |. E8 E300F9FF                                        CALL update.00402A44
00472961  |. 8B45 EC                                            MOV EAX,DWORD PTR SS:[EBP-14]
00472964  |. 8D55 F0                                            LEA EDX,DWORD PTR SS:[EBP-10]
00472967  |. E8 3866F9FF                                        CALL update.00408FA4
0047296C  |. 8D45 F0                                            LEA EAX,DWORD PTR SS:[EBP-10]
0047296F  |. BA 702A4700                                        MOV EDX,update.00472A70                       ;  ASCII "patch.exe"
00472974  |. E8 F71EF9FF                                        CALL update.00404870
00472979  |. 8B45 F0                                            MOV EAX,DWORD PTR SS:[EBP-10]
0047297C  |. E8 8B65F9FF                                        CALL update.00408F0C
00472981  |. 837D F8 00                                         CMP DWORD PTR SS:[EBP-8],0
00472985  |. 75 29                                              JNZ SHORT update.004729B0
00472987  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
0047298A  |. 8B80 28030000                                      MOV EAX,DWORD PTR DS:[EAX+328]
00472990  |. 8B55 FC                                            MOV EDX,DWORD PTR SS:[EBP-4]
00472993  |. 3B82 2C030000                                      CMP EAX,DWORD PTR DS:[EDX+32C]
00472999  |. 7D 47                                              JGE SHORT update.004729E2
0047299B  |. B2 01                                              MOV DL,1
0047299D  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004729A0  |. 8B80 10030000                                      MOV EAX,DWORD PTR DS:[EAX+310]
004729A6  |. E8 3970FBFF                                        CALL update.004299E4
004729AB  |. E9 92000000                                        JMP update.00472A42
004729B0  |> 837D F8 05                                         CMP DWORD PTR SS:[EBP-8],5
004729B4  |. 75 17                                              JNZ SHORT update.004729CD
004729B6  |. 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
004729B8  |. 66:8B0D 7C2A4700                                   MOV CX,WORD PTR DS:[472A7C]                   ; |
004729BF  |. 33D2                                               XOR EDX,EDX                                   ; |
004729C1  |. B8 882A4700                                        MOV EAX,update.00472A88                       ; |ASCII "Patch cancelled.  Your game client may be out of date and not function properly."
004729C6  |. E8 A51CFEFF                                        CALL update.00454670                          ; \update.00454670
004729CB  |. EB 15                                              JMP SHORT update.004729E2
004729CD  |> 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
004729CF  |. 66:8B0D 7C2A4700                                   MOV CX,WORD PTR DS:[472A7C]                   ; |
004729D6  |. 33D2                                               XOR EDX,EDX                                   ; |
004729D8  |. B8 E42A4700                                        MOV EAX,update.00472AE4                       ; |ASCII "Patch failed.  Your game client may be out of date and not function properly."
004729DD  |. E8 8E1CFEFF                                        CALL update.00454670                          ; \update.00454670
004729E2  |> 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004729E5  |. 8B80 40030000                                      MOV EAX,DWORD PTR DS:[EAX+340]
004729EB  |. 50                                                 PUSH EAX                                      ; /hObject
004729EC  |. E8 073FF9FF                                        CALL <JMP.&kernel32.CloseHandle>              ; \CloseHandle
004729F1  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
004729F4  |. E8 3FECFFFF                                        CALL update.00471638
004729F9  |. E8 361AF9FF                                        CALL update.00404434
004729FE  |. EB 42                                              JMP SHORT update.00472A42
00472A00  |> 6A 00                                              PUSH 0                                        ; /ExitCode = 0
00472A02  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]                  ; |
00472A05  |. 8B80 40030000                                      MOV EAX,DWORD PTR DS:[EAX+340]                ; |
00472A0B  |. 50                                                 PUSH EAX                                      ; |hProcess
00472A0C  |. E8 2741F9FF                                        CALL <JMP.&kernel32.TerminateProcess>         ; \TerminateProcess
00472A11  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472A14  |. 8B80 40030000                                      MOV EAX,DWORD PTR DS:[EAX+340]
00472A1A  |. 50                                                 PUSH EAX                                      ; /hObject
00472A1B  |. E8 D83EF9FF                                        CALL <JMP.&kernel32.CloseHandle>              ; \CloseHandle
00472A20  |. 6A 00                                              PUSH 0                                        ; /Arg1 = 00000000
00472A22  |. 66:8B0D 7C2A4700                                   MOV CX,WORD PTR DS:[472A7C]                   ; |
00472A29  |. 33D2                                               XOR EDX,EDX                                   ; |
00472A2B  |. B8 E42A4700                                        MOV EAX,update.00472AE4                       ; |ASCII "Patch failed.  Your game client may be out of date and not function properly."
00472A30  |. E8 3B1CFEFF                                        CALL update.00454670                          ; \update.00454670
00472A35  |. 8B45 FC                                            MOV EAX,DWORD PTR SS:[EBP-4]
00472A38  |. E8 FBEBFFFF                                        CALL update.00471638
00472A3D  |. E8 F219F9FF                                        CALL update.00404434
00472A42  |> 33C0                                               XOR EAX,EAX
00472A44  |. 5A                                                 POP EDX
00472A45  |. 59                                                 POP ECX
00472A46  |. 59                                                 POP ECX
00472A47  |. 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00472A4A  |. 68 642A4700                                        PUSH update.00472A64
00472A4F  |> 8D45 EC                                            LEA EAX,DWORD PTR SS:[EBP-14]
00472A52  |. BA 02000000                                        MOV EDX,2
00472A57  |. E8 701BF9FF                                        CALL update.004045CC
00472A5C  \. C3                                                 RETN
00472A5D   .^E9 C614F9FF                                        JMP update.00403F28
00472A62   .^EB EB                                              JMP SHORT update.00472A4F
00472A64   . 8BE5                                               MOV ESP,EBP
00472A66   . 5D                                                 POP EBP
00472A67   . C3                                                 RETN
00472A68   . FFFFFFFF                                           DD FFFFFFFF
00472A6C   . 09000000                                           DD 00000009
00472A70   . 70 61 74 63 68 2E 65 78 65 00                      ASCII "patch.exe",0
00472A7A     00                                                 DB 00
00472A7B     00                                                 DB 00
00472A7C   . 0400                                               DW 0004
00472A7E     00                                                 DB 00
00472A7F     00                                                 DB 00
00472A80   . FFFFFFFF                                           DD FFFFFFFF
00472A84   . 50000000                                           DD 00000050
00472A88   . 50 61 74 63 68 20 63 61 6E 63 65 6C 6C 65 64 2E    ASCII "Patch cancelled."
00472A98   . 20 20 59 6F 75 72 20 67 61 6D 65 20 63 6C 69 65    ASCII "  Your game clie"
00472AA8   . 6E 74 20 6D 61 79 20 62 65 20 6F 75 74 20 6F 66    ASCII "nt may be out of"
00472AB8   . 20 64 61 74 65 20 61 6E 64 20 6E 6F 74 20 66 75    ASCII " date and not fu"
00472AC8   . 6E 63 74 69 6F 6E 20 70 72 6F 70 65 72 6C 79 2E    ASCII "nction properly."
00472AD8   . 00                                                 ASCII 0
00472AD9     00                                                 DB 00
00472ADA     00                                                 DB 00
00472ADB     00                                                 DB 00
00472ADC   . FFFFFFFF                                           DD FFFFFFFF
00472AE0   . 4D000000                                           DD 0000004D
00472AE4   . 50 61 74 63 68 20 66 61 69 6C 65 64 2E 20 20 59    ASCII "Patch failed.  Y"
00472AF4   . 6F 75 72 20 67 61 6D 65 20 63 6C 69 65 6E 74 20    ASCII "our game client "
00472B04   . 6D 61 79 20 62 65 20 6F 75 74 20 6F 66 20 64 61    ASCII "may be out of da"
00472B14   . 74 65 20 61 6E 64 20 6E 6F 74 20 66 75 6E 63 74    ASCII "te and not funct"
00472B24   . 69 6F 6E 20 70 72 6F 70 65 72 6C 79 2E 00          ASCII "ion properly.",0
00472B32     00                                                 DB 00
00472B33     00                                                 DB 00
00472B34   . 55                                                 PUSH EBP
00472B35   . 8BEC                                               MOV EBP,ESP
00472B37   . 33C0                                               XOR EAX,EAX
00472B39   . 55                                                 PUSH EBP
00472B3A   . 68 592B4700                                        PUSH update.00472B59
00472B3F   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
00472B42   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00472B45   . FF05 4C6F4700                                      INC DWORD PTR DS:[476F4C]
00472B4B   . 33C0                                               XOR EAX,EAX
00472B4D   . 5A                                                 POP EDX
00472B4E   . 59                                                 POP ECX
00472B4F   . 59                                                 POP ECX
00472B50   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00472B53   . 68 602B4700                                        PUSH update.00472B60
00472B58   > C3                                                 RETN                                          ;  RET used as a jump to 00472B60
00472B59   .^E9 CA13F9FF                                        JMP update.00403F28
00472B5E   .^EB F8                                              JMP SHORT update.00472B58
00472B60   > 5D                                                 POP EBP
00472B61   . C3                                                 RETN
00472B62     8BC0                                               MOV EAX,EAX
00472B64   . 832D 4C6F4700 01                                   SUB DWORD PTR DS:[476F4C],1
00472B6B   . C3                                                 RETN
00472B6C  /$ 55                                                 PUSH EBP
00472B6D  |. 8BEC                                               MOV EBP,ESP
00472B6F  |. 83C4 F8                                            ADD ESP,-8
00472B72  |. 68 AC2B4700                                        PUSH update.00472BAC                          ; /MapName = "LRUpdateClientMapFile"
00472B77  |. 6A 20                                              PUSH 20                                       ; |MaximumSizeLow = 20
00472B79  |. 6A 00                                              PUSH 0                                        ; |MaximumSizeHigh = 0
00472B7B  |. 6A 02                                              PUSH 2                                        ; |Protection = PAGE_READONLY
00472B7D  |. 6A 00                                              PUSH 0                                        ; |pSecurity = NULL
00472B7F  |. 6A FF                                              PUSH -1                                       ; |hFile = FFFFFFFF
00472B81  |. E8 923DF9FF                                        CALL <JMP.&kernel32.CreateFileMappingA>       ; \CreateFileMappingA
00472B86  |. 8945 F8                                            MOV DWORD PTR SS:[EBP-8],EAX
00472B89  |. 837D F8 00                                         CMP DWORD PTR SS:[EBP-8],0
00472B8D  |. 74 12                                              JE SHORT update.00472BA1
00472B8F  |. E8 643EF9FF                                        CALL <JMP.&kernel32.GetLastError>             ; [GetLastError
00472B94  |. 3D B7000000                                        CMP EAX,0B7
00472B99  |. 75 06                                              JNZ SHORT update.00472BA1
00472B9B  |. C645 FF 00                                         MOV BYTE PTR SS:[EBP-1],0
00472B9F  |. EB 04                                              JMP SHORT update.00472BA5
00472BA1  |> C645 FF 01                                         MOV BYTE PTR SS:[EBP-1],1
00472BA5  |> 8A45 FF                                            MOV AL,BYTE PTR SS:[EBP-1]
00472BA8  |. 59                                                 POP ECX
00472BA9  |. 59                                                 POP ECX
00472BAA  |. 5D                                                 POP EBP
00472BAB  \. C3                                                 RETN
00472BAC   . 4C 52 55 70 64 61 74 65 43 6C 69 65 6E 74 4D 61    ASCII "LRUpdateClientMa"
00472BBC   . 70 46 69 6C 65 00                                  ASCII "pFile",0
00472BC2     00                                                 DB 00
00472BC3     00                                                 DB 00
00472BC4  /$ 55                                                 PUSH EBP
00472BC5  |. 8BEC                                               MOV EBP,ESP
00472BC7  |. 83C4 F8                                            ADD ESP,-8
00472BCA  |. 68 042C4700                                        PUSH update.00472C04                          ; /MapName = "LRClientMapFile"
00472BCF  |. 6A 20                                              PUSH 20                                       ; |MaximumSizeLow = 20
00472BD1  |. 6A 00                                              PUSH 0                                        ; |MaximumSizeHigh = 0
00472BD3  |. 6A 02                                              PUSH 2                                        ; |Protection = PAGE_READONLY
00472BD5  |. 6A 00                                              PUSH 0                                        ; |pSecurity = NULL
00472BD7  |. 6A FF                                              PUSH -1                                       ; |hFile = FFFFFFFF
00472BD9  |. E8 3A3DF9FF                                        CALL <JMP.&kernel32.CreateFileMappingA>       ; \CreateFileMappingA
00472BDE  |. 8945 F8                                            MOV DWORD PTR SS:[EBP-8],EAX
00472BE1  |. 837D F8 00                                         CMP DWORD PTR SS:[EBP-8],0
00472BE5  |. 74 12                                              JE SHORT update.00472BF9
00472BE7  |. E8 0C3EF9FF                                        CALL <JMP.&kernel32.GetLastError>             ; [GetLastError
00472BEC  |. 3D B7000000                                        CMP EAX,0B7
00472BF1  |. 75 06                                              JNZ SHORT update.00472BF9
00472BF3  |. C645 FF 00                                         MOV BYTE PTR SS:[EBP-1],0
00472BF7  |. EB 04                                              JMP SHORT update.00472BFD
00472BF9  |> C645 FF 01                                         MOV BYTE PTR SS:[EBP-1],1
00472BFD  |> 8A45 FF                                            MOV AL,BYTE PTR SS:[EBP-1]
00472C00  |. 59                                                 POP ECX
00472C01  |. 59                                                 POP ECX
00472C02  |. 5D                                                 POP EBP
00472C03  \. C3                                                 RETN
00472C04   . 4C 52 43 6C 69 65 6E 74 4D 61 70 46 69 6C 65 00    ASCII "LRClientMapFile",0
00472C14  /$ 55                                                 PUSH EBP
00472C15  |. 8BEC                                               MOV EBP,ESP
00472C17  |. 83C4 F8                                            ADD ESP,-8
00472C1A  |. 68 542C4700                                        PUSH update.00472C54                          ; /MapName = "LREditorMapFile"
00472C1F  |. 6A 20                                              PUSH 20                                       ; |MaximumSizeLow = 20
00472C21  |. 6A 00                                              PUSH 0                                        ; |MaximumSizeHigh = 0
00472C23  |. 6A 02                                              PUSH 2                                        ; |Protection = PAGE_READONLY
00472C25  |. 6A 00                                              PUSH 0                                        ; |pSecurity = NULL
00472C27  |. 6A FF                                              PUSH -1                                       ; |hFile = FFFFFFFF
00472C29  |. E8 EA3CF9FF                                        CALL <JMP.&kernel32.CreateFileMappingA>       ; \CreateFileMappingA
00472C2E  |. 8945 F8                                            MOV DWORD PTR SS:[EBP-8],EAX
00472C31  |. 837D F8 00                                         CMP DWORD PTR SS:[EBP-8],0
00472C35  |. 74 12                                              JE SHORT update.00472C49
00472C37  |. E8 BC3DF9FF                                        CALL <JMP.&kernel32.GetLastError>             ; [GetLastError
00472C3C  |. 3D B7000000                                        CMP EAX,0B7
00472C41  |. 75 06                                              JNZ SHORT update.00472C49
00472C43  |. C645 FF 00                                         MOV BYTE PTR SS:[EBP-1],0
00472C47  |. EB 04                                              JMP SHORT update.00472C4D
00472C49  |> C645 FF 01                                         MOV BYTE PTR SS:[EBP-1],1
00472C4D  |> 8A45 FF                                            MOV AL,BYTE PTR SS:[EBP-1]
00472C50  |. 59                                                 POP ECX
00472C51  |. 59                                                 POP ECX
00472C52  |. 5D                                                 POP EBP
00472C53  \. C3                                                 RETN
00472C54   . 4C 52 45 64 69 74 6F 72 4D 61 70 46 69 6C 65 00    ASCII "LREditorMapFile",0
00472C64   . 55                                                 PUSH EBP
00472C65   . 8BEC                                               MOV EBP,ESP
00472C67   . 33C0                                               XOR EAX,EAX
00472C69   . 55                                                 PUSH EBP
00472C6A   . 68 832C4700                                        PUSH update.00472C83
00472C6F   . 64:FF30                                            PUSH DWORD PTR FS:[EAX]
00472C72   . 64:8920                                            MOV DWORD PTR FS:[EAX],ESP
00472C75   . 33C0                                               XOR EAX,EAX
00472C77   . 5A                                                 POP EDX
00472C78   . 59                                                 POP ECX
00472C79   . 59                                                 POP ECX
00472C7A   . 64:8910                                            MOV DWORD PTR FS:[EAX],EDX
00472C7D   . 68 8A2C4700                                        PUSH update.00472C8A
00472C82   > C3                                                 RETN                                          ;  RET used as a jump to 00472C8A
00472C83   .^E9 A012F9FF                                        JMP update.00403F28
00472C88   .^EB F8                                              JMP SHORT update.00472C82
00472C8A   > 5D                                                 POP EBP
00472C8B   . C3                                                 RETN
00472C8C     68                                                 DB 68                                         ;  CHAR 'h'
00472C8D     00                                                 DB 00
00472C8E     00                                                 DB 00
00472C8F     00                                                 DB 00

