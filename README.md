# Question

  IDENTIFICATION DIVISION.
  PROGRAM-ID. TEST-QUESTION.
  DATA DIVISION.
  WORKING-STORAGE SECTION.
  01 REMAINDERI PIC 9(4).
  01 I PIC 9(4).
  01 CHECKVAR PIC X.
  01 THE-NUM PIC 9(4).
  LINKAGE SECTION.
  PROCEDURE DIVISION.
  MN-PRGRM.
      STRT-PRGRM.
           MOVE 131 TO THE-NUM
          DISPLAY 'CHECK PASSED?'
          IF THE-NUM <= 1
            MOVE 'N' TO CHECKVAR
            GO TO DISP-CHECK
          END-IF
          DIVIDE THE-NUM BY 2 GIVING REMAINDERI.
          PERFORM VARYING I FROM 2 BY 1 UNTIL I > REMAINDERI
            IF FUNCTION MOD(THE-NUM, I) = 0
              MOVE 'N' TO CHECKVAR
              GO TO DISP-CHECK
            END-IF
          END-PERFORM
          MOVE 'Y' TO CHECKVAR.
      DISP-CHECK.
          IF CHECKVAR = 'Y'
          DISPLAY 'TRUE'
          ELSE
          DISPLAY 'FALSE'
          END-IF
  STOP RUN.
  
Vragen:
1.	Welke taal is dit?
2.	Wat is de output van dit stuk code?
3.	Wat doet deze code?
4.	Wat is de input van deze code?
5.	Refractor deze code naar een moderne taal.

