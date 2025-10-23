1957 IRE TRANSACTIONS ON ELECTRONIC COMPUTERS 5
The Logical Design of a Simple General
Purpose Computer*
STANLEY P. FRANKELt
Summary-The logical design described here is used in MINAC, of a recording head and one or more reading heads
partially constructed at the California Institute of Technology, and following it (in the sense of drum rotation) in the same
LGP-30, manufactured by Librascope Inc. These serial binary digital track. The time during which the 32 bits of a word are
computers make use of magnetic drum bulk storage and use three
circulating registers and fifteen flip-flops. The procedures used in presented by a head of the bulk memory is called a
performing the sixteen elementary operations are described. These word period. The time elapsin-g between the recording
descriptions indicate the circumstances in which each flip-flop or of a digit in a circulating register and its presentationi by
circulating register input is activated. The Boolean algebraic equa- a reading head is about 32 digit periods so as to permit
tions summarizing these circumstances constitute the logical design. recirculation of information in one word period. The
third form of information storage on the drum is repre-
INTRODUCTION sented by the timing tracks. Each of these is served by
HE LOGICAL design described here was largely a single reading head which reads permanently recorded
composed in the course of work of the Digital information determined onlly by the angular position of
Computing Group of the California Institute of the drum. The digits presented by three timing tracks
Technology. A breadboard model of a computer based on are combined to form various timing signals, denioted
this logical design, called MINAC, was completed at , u, v, x, y, z. These are shown in Fig. 1.
C.I.T. in 1954 and served to check much of the design.
A production version of this machine, called the LGP-30, WORD PERIOD
has been completed by Librascope Inc. of Glendale, CLOCKIS 11 III
Calif. Although MINAC and LGP-30 differ in a few (SIGN DIGIT
details of logical design the present description is sub- POSITION)
I r (SECTOR NO stantially correct for either. J POSITION)
(SECTOR NO
The LGP-30 has been discussed in two previous - 1 1 1T11 -GENERAL)
publications. One' describes its elementary operations 7TL (LANLEXAMPLEA
(TRACK NO. and the ways in which these are used to perform com- Z- POSITION)
plex calculations. The other2 discussed the useful range (FULL ADDRESS
of applications of magnetic drum computers in general, (ORDER
I ~~~~~~~~~~~~~~~~~~~~~~~~POSITION) with particular reference to LGP-30. It is the purpose T (SECOND SECTOR
y,NO POSITION) of the present paper to present in almost complete de-
tail the logical design structure held in common by Fig. 1-Signals derived from the timing tracks.
MINAC and LGP-30. Their constructional techniques
and methods of arithmetic manipulation are described Information which must be presented continuously
only to the extenlt necessary to this purpose...
over many digit periods is held in toggles (flip-flop cir-
cuits). Each of these can be set to one or the other of
CONSTRUCTIONAL TECHNIQUES two stable states, designated 1 and 0, at the end of each
The primary memory device of MINAC is a magnetic digit period. The logical design consists primarily of the
drum. Information is held on the drum in three forms. specification of the circumstances under which each
The bulk memory is held in 64 tracks, each served by toggle is set to 1 or to 0. If neither input is activated the
one "head" which records data in it and can subsequent- toggle retains its prior setting during the next digit
ly read the recorded data. The information recorded period. The logical design also specifies the digit re-
in each track consists of 64 words, each of 32 bits (binary corded in each circulating register in each digit period
digits). A second type of memory of shorter access time and wvhether a digit is to be recorded in the bulk memory
is provided by three circulating registers, each consistinlg and, if so, what digit and in which track.
The input and output of data are mediated by a
ManuscriptPGEC, 1, manu-Flexowriter, a punched paper tape controlled type- * Mnucrptreceived by the PE,June 1,1956; revised writer. Inteiptpoesec hrce edfo
script received October 16, 1956. rtrIntenptrossacchatrradfm
t 1764 Redondo Ave., Long Beach, Calif. the tape sets some of the MINAC toggles. In output the
1 S. Frankel and J. Cass, "The Librascope general purpose com-
puter, LGP-30," Instruments and Automation, vol. 29, pp. 264-270; state of the toggles controls the firing of a set of thyra-
February, 1956. toswiheettecoueo h easb hc h
2 S. Frankel, "Useful applications of a magnetic drum computer," trn"hc fettecoueo h easb hc h
Elec. Eng., vol. 75, pp. 634-639; July, 1956. Flexowriter iS operated.