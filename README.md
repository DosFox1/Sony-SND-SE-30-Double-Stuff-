# Sony-SND-SE-30-Double-Stuff
BETA - A replacement for the Sony SND IC (part number 343-0045-A), specifically designed for the SE/30.
This design is a duplication of the previous Sony SND SMD version, but literally copied twice to fit two Sony SNDs onto the board without the DRC yelling at me.

<img width="721" height="603" alt="image" src="https://github.com/user-attachments/assets/0d459273-204f-4142-908c-e66461c794e4" />
<img width="717" height="602" alt="image" src="https://github.com/user-attachments/assets/445fca35-122e-4e93-bd10-2416c299c860" />


# So What Is It?
This is quite literally the same design as before, with the same improvement of not needing the -12V rail. 
However, due to the board constraints of the SE/30, two of my SMD boards will not fit - at least easily. 
So this design just adds a second SND replacement so the DRC doesn't yell at me. 

It's all common jellybean parts, so nothing hyper specific is needed.


**Please note that -12V will need to be tapped from somewhere on the board, otherwise the audio doesn't work.**

**Also the 27R Pullup resistor at R11 on the logic board needs to be removed, otherwise POR doesn't work!**

The original SMD Design is here:
https://github.com/DosFox1/Sony-SND-SMT-Replacement

And the very original THT design is here:
https://github.com/DosFox1/Sony-SND-THT-Replacement

**Please Also Note That This Is Completely Untested, Build At Your Own Risk**

# Bill Of Materials:

```blocks
Part     Value          Device                       Package  Library                Sheet

C1       100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C2       100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C3       100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C4       100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C5       1u 16V         1U_CAP_0603                  C0603    Capacitors SMD         1
C6       100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C7       470p           100P_CAP_0603                C0603    Capacitors SMD         1
C8       1n 50V         10N_CAP_0603                 C0603    Capacitors SMD         1
C9       100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C10      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C11      220p           100P_CAP_0603                C0603    Capacitors SMD         1
C12      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C13      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C14      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C15      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C16      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C17      470p           100P_CAP_0603                C0603    Capacitors SMD         1
C18      1n 50V         10N_CAP_0603                 C0603    Capacitors SMD         1
C19      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C20      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C21      220p           100P_CAP_0603                C0603    Capacitors SMD         1
C22      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
C23      1u 16V         1U_CAP_0603                  C0603    Capacitors SMD         1
C24      100n 16V       100N_CAP_0603                C0603    Capacitors SMD         1
D1       5.1V           DIODE-ZENER-MMSZ5232BS       SOD-123  SparkFun-DiscreteSemi  1
D2       5.1V           DIODE-ZENER-MMSZ5232BS       SOD-123  SparkFun-DiscreteSemi  1
IC1      TL072          OPAMP-DUALU                  SO08     SparkFun-IC-Amplifiers 1
IC2      4016D          4016D                        SO14     40xx                   1
IC3      NE555DRG4      555_SOIC8                    SOIC8    ICs                    1
IC4      74LVC1G06DBV   74LVC1G06DBV                 SOT23-5  74xx-little-us         1
IC5      Turned Pins    SND Turned Pins              DIP16    Pins                   1
IC6      4016D          4016D                        SO14     40xx                   1
IC7      Turned Pins    SND Turned Pins              DIP16    ICs                    1
IC8      74LVC1G06DBV   74LVC1G06DBV                 SOT23-5  74xx-little-us         1
IC9      NE555DRG4      555_SOIC8                    SOIC8    Pins                   1
IC10     TL072          OPAMP-DUALU                  SO08     SparkFun-IC-Amplifiers 1
Q1       MMBT3906       TRANS_PNP-PMBT3906|MMBT3906L SOT23-3  SparkFun-DiscreteSemi  1
Q2       MMBT3904       TRANS_NPN-MMBT2222AL         SOT23-3  SparkFun-DiscreteSemi  1
Q3       MMBT3906       TRANS_PNP-PMBT3906|MMBT3906L SOT23-3  SparkFun-DiscreteSemi  1
Q4       MMBT3904       TRANS_NPN-MMBT2222AL         SOT23-3  SparkFun-DiscreteSemi  1
R1       1M             GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R2       1M             GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R3       6K8            GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R4       47K            47K_RESISTOR                 R0603    Resistors SMD          1
R5       1k             1K_RESISTOR_0603             R0603    Resistors SMD          1
R6       47K            47K_RESISTOR                 R0603    Resistors SMD          1
R7       68K            GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R8       150K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R9       470K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R10      470K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R11      200K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R12      150R           150R_RESISTOR_0603           R0603    Resistors SMD          1
R13      47K            47K_RESISTOR                 R0603    Resistors SMD          1
R14      47K            47K_RESISTOR                 R0603    Resistors SMD          1
R15      1M             GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R16      1M             GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R17      1k             1K_RESISTOR_0603             R0603    Resistors SMD          1
R18      6K8            GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R19      68K            GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R20      150K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R21      470K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R22      470K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R23      200K           GENERIC_RESISTOR_0603        R0603    Resistors SMD          1
R24      150R           150R_RESISTOR_0603           R0603    Resistors SMD          1

```

