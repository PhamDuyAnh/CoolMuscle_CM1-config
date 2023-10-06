CoolMuscle CM1 motor, CoolWorks Lite v4.1.7.4
Serial config: paud 38400
Current motor: 2
-->
Motor Pin:
01 - 24V +
02 - 24V gnd
03 -                     In 2-  CCW-          (TLP115 opto)
04 -                     Ou 2   Alarm
05 - Rx  (FT232)         Ou 1   Inposition
06 -                     In 4                 (pull up + Analog In)
07 -                     In 3   Disable       (pull up)
08 - Gnd (FT232)         In 1-  CW-
09 -                     In 2+  CCW+
10 - Tx  (FT232)         In 1+  CW+
11 - Gnd (FT232)
12 - 5V+ (Out)
-->
!  - CMD to reset default
CoolMuscle
 S Version:V0.205
 H Version:V4.00
 Serial No:1 
-->
?90.2
K25=3333    ,K26=0000    ,K27=0000    ,K28=0100    
K29=0000    ,K30=0000    ,K31=0200    ,K32=0300    
K33=11      ,K34=21      ,K35=31      ,K36=1       
K37=4       ,K38=0       ,K39=128     ,K40=3000    
K41=2000    ,K42=2000    ,K43=100     ,K44=100     
K45=1       ,K46=0       ,K47=30      ,K48=0       
K49=10      ,K50=10      ,K51=10      ,K52=5       
K53=201     ,K54=1       ,K55=5       ,K56=5000    
K57=10000   ,K58=0       ,K59=0       ,K60=30      
K61=200     ,K62=0       ,K63=0       ,K64=0  

K1 =0
K2 =2024
K3 =3000    - Maximum speed
K4 =200
K5 =250
K6 =70
K7 =0
K8 =175
K9 =1400
K10=11
K11=0
K12=7
K13=1       - Product category
K14=20      - Communication Echo (defaulu = 0)
K15=0       
K16=2       - Inteface type (MODE: 0 sets motor to a P – type, 1 sets motor to a V – type, 2 sets motor to a C - type)
K17=80      
K18=6       
K19=1238    - Serial No
K20=0       - BaudRate
K21=0       - Closed loop mode (0 is full closed loop)
K22=0       - time delay for semi-closed loop
K23=0       
K24=0

-->> KOLEKTOR-servopohony-Reliance-Cool-Muscle-manual
Gain, value 1-300
K52=50    | Position P gain 
K53=250   | Velocity P gain
K54=1     | Velocity I gain

In ‘Single Line Command’ you have to enter in this order:
- w=526 (is a Agent password)
- K16=2 (2 - C type)
- ?K16 (testing if motor has stored new value).
After each entry you have to press enter! At last you should power down the motor
and then back on. Then try to run a bank.
The procedure to switch back to P – type is the same except K16=2 you use K16=0.
Available values for K16 are :
0 sets motor to a P – type
1 sets motor to a V – type
2 sets motor to a C - type

W=526
K16=0       //0: P – type, 1: V – type, 2: C - type
K36=1       //0: CW/CCW, 1: Pulse / Direction, 2: Enable to execute Program Banks 2 and 3 (except for C type)
$

W=526
K16=1       //0: P – type, 1: V – type, 2: C - type
K38=2       //Analog Control Type 1: Position control, 2 or 3: CW/CCW speed control
K40=2000    //Maximum Speed
$

W=526
K16=1       //0: P – type, 1: V – type, 2: C - type
K38=2       //Analog Control Type 1: Position control, 2 or 3: CW/CCW speed control
K41=1000    //Analog Travel range (-32767 -> 32767)
$

W=526
K16=2       //0: P – type, 1: V – type, 2: C - type
K28=9800    //Input Function at Rising Edge of Quick Response Signal
K36=2       //0: CW/CCW, 1: Pulse / Direction, 2: Enable to execute Program Banks 2 and 3 (except for C type)
$



%85.1
K0 =885  ,iaOffset=524  ,ibOffset=522  ,K252=455  ,K253=468  ,K254=875  ,K255=23205
W=885 (what is a Muscle password)
%85.1
K0=924,iaOffset=524,ibOffset=524,K1020=522,K1021=507,K1022=268,K1023=5AA5
W=924 (what is a Muscle password)

?90.1
K20.1=0     ,K21.1=0     ,K22.1=200   ,K23.1=1     
K24.1=1000  ,K25.1=3333  ,K26.1=0000  ,K27.1=0000  
K28.1=1687  ,K29.1=0000  ,K30.1=0000  ,K31.1=0000  
K32.1=0000  ,K33.1=11    ,K34.1=21    ,K35.1=30    
K36.1=2     ,K37.1=3     ,K38.1=1     ,K39.1=128   
K40.1=200   ,K41.1=2000  ,K42.1=30    ,K43.1=100   
K44.1=100   ,K45.1=1     ,K46.1=1     ,K47.1=30    
K48.1=5     ,K49.1=10    ,K50.1=10    ,K51.1=10    
K52.1=150   ,K53.1=150   ,K54.1=5     ,K55.1=5     
K56.1=50    ,K57.1=3000  ,K58.1=0     ,K59.1=0     
K60.1=50    ,K61.1=200   ,K62.1=0     ,K63.1=0     
K64.1=0     ,K65.1=0     ,K66.1=0     ,K67.1=1     
K68.1=0     ,K69.1=0     ,K70.1=1     ,K71.1=100   
K72.1=300   ,K73.1=10    ,K74.1=0     ,K75.1=0     
K76.1=0     ,K77.1=0     ,K78.1=0     ,K79.1=0     
K80.1=0     ,K81.1=0     ,K82.1=0     ,K83.1=0     
K84.1=0  

K1
K2
K3
K4
K5
K6
K7
K8
K9
K10
K11
K12
K13
K14
K15
K16
K17
K18
K19
K20
K21
K22
K23
K24
K25
K26
K27
K28
K29
K30
K31
K32
K33
K34
K35
K36
K37
K38
K39
K40
K41
K42
K43
K44
K45
K46
K47
K48
K49
K50
K51
K52
K53
K54
K55
K56
K57
K58
K59
K60
K61
K62
K63
K64




|2.1
p.1=1000,s=100,a=1
^.1


%85.1
%85.1
K0 =885  ,iaOffset=524  ,ibOffset=522  ,K252=455  ,K253=468  ,K254=875  ,K255=23205
W=885
?87
W=885

?87

K1 =0       ,K2 =2024    ,K3 =3000    ,K4 =200     

K5 =250     ,K6 =70      ,K7 =-14     ,K8 =175     

K9 =1400    ,K10=11      ,K11=0       ,K12=7       

K13=1       ,K14=0       ,K15=526     ,K16=2       

K17=80      ,K18=6       ,K19=1       ,K20=0       

K21=0       ,K22=0       ,K23=0       ,K24=0       

K25=3333    ,K26=0000    ,K27=0000    ,K28=6600    

K29=0000    ,K30=0000    ,K31=0000    ,K32=0000    

K33=11      ,K34=21      ,K35=30      ,K36=1       

K37=4       ,K38=1       ,K39=128     ,K40=200     

K41=2000    ,K42=30      ,K43=100     ,K44=100     

K45=1       ,K46=0       ,K47=30      ,K48=5       

K49=10      ,K50=10      ,K51=10      ,K52=200     

K53=200     ,K54=1       ,K55=5       ,K56=50      

K57=3000    ,K58=0       ,K59=0       ,K60=50      

K61=200     ,K62=0       ,K63=0       ,K64=0       

W.1=0
W.1=0

?99.1
?99.1

Ux=8

]
?85.1
]
?85.1
 
?

K2
K2

K2 =2024    

K19
K19

K19=1       

%84.1
%84.1
maxAxisNo=1 

%100.1
%100.1

?87.1
?87.1

K1 =0       ,K2 =2024    ,K3 =3000    ,K4 =200     

K5 =250     ,K6 =70      ,K7 =-14     ,K8 =175     

K9 =1400    ,K10=11      ,K11=0       ,K12=7       

K13=1       ,K14=0       ,K15=0       ,K16=2       

K17=80      ,K18=6       ,K19=1       ,K20=0       

K21=0       ,K22=0       ,K23=0       ,K24=0       

K25=3333    ,K26=0000    ,K27=0000    ,K28=6600    

K29=0000    ,K30=0000    ,K31=0000    ,K32=0000    

K33=11      ,K34=21      ,K35=30      ,K36=1       

K37=4       ,K38=1       ,K39=128     ,K40=200     

K41=2000    ,K42=30      ,K43=100     ,K44=100     

K45=1       ,K46=0       ,K47=30      ,K48=5       

K49=10      ,K50=10      ,K51=10      ,K52=200     

K53=200     ,K54=1       ,K55=5       ,K56=50      

K57=3000    ,K58=0       ,K59=0       ,K60=50      

K61=200     ,K62=0       ,K63=0       ,K64=0       

?91.1
?91.1

P1 =11111     ,P2 =22222     ,P3 =33333     ,P4 =0         

P5 =0         ,P6 =0         ,P7 =0         ,P8 =0         

P9 =0         ,P10=0         ,P11=0         ,P12=0         

P13=0         ,P14=0         ,P15=0         ,P16=0         

P17=0         ,P18=0         ,P19=0         ,P20=0         

P21=0         ,P22=0         ,P23=0         ,P24=0         

P25=0         

?92.1
?92.1

S1 =200  ,S2 =200  ,S3 =200  ,S4 =0    

S5 =0    ,S6 =0    ,S7 =0    ,S8 =0    

S9 =0    ,S10=0    ,S11=0    ,S12=0    

S13=0    ,S14=0    ,S15=0    

?93.1
?93.1

A1 =100  ,A2 =100  ,A3 =100  ,A4 =0    

A5 =0    ,A6 =0    ,A7 =0    ,A8 =0    

?94.1
?94.1

T1 =0    ,T2 =0    ,T3 =0    ,T4 =0    

T5 =0    ,T6 =0    ,T7 =0    

?.1
?.1

P0=1000      ,S0=100  ,A0=100  

%87.1
%87.1

?1.1
?1.1

I3, C2, C4

I4, C3, C4

?2.1
?2.1

A2

S2

P2

?3.1
?3.1

A3

S3

P3

?4.1
?4.1

?5.1
?5.1

?6.1
?6.1

?7.1
?7.1

?8.1
?8.1

?9.1
?9.1

?10.1
?10.1

?11.1
?11.1

?12.1
?12.1

?13.1
?13.1

?14.1
?14.1

?15.1
?15.1

