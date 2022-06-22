# CECS 326 Reading Assignment: Input and Output
## 20 points

### Assignment Description
Answer the following questions from the Chapter 5 reading from your textbook. Be complete with your answers. You may work on these questions with one or two other partners, but *all* students must submit the document individually in their own repositories along with each student's name documented with the submission.

1. A DMA controller has five channels. The controller is capable of requesting a 32-bit word every 40 nsec. A response takes equally long. How fast does the bus have to be to avoid being a bottleneck?

2. Explain how an OS can facilitate installation of a new device without any need for recompiling the OS.

3. Why are output files for the printer normally spooled on disk before being printed?

4. What are the advantages and disadvantages of optical disks versus magnetic disks?

5. A computer manufacturer decides to redesign the partition table of a Pentium hard disk to provide more than four partitions. What are some consequences of this change?

6. After receiving a **SIGINT** character, the display driver discards all output currently queued for that display. Why?

7. Many versions of UNIX use an unsigned 32-bit integer to keep track of the time as the number of seconds since the origin of time. When will these systems wrap around (year and month)? Do you expect this to actually happen?

8. Disk requests come in to the disk driver for cylinders 10, 22, 20, 2, 40, 6, and 38, in that order. A seek takes *6 msec* per cylinder.
    How much seek time is needed for:
        a. First-come, first served
        b. Closest cylinder next
        c. Elevator algorithm (initially moving upward)
    In all cases, the arm is initially at cylinder 20.

9. Describe two advantages and two disadvantages of thin client computing?

10. A notebook computer is set up to take maximum advantage of power saving features including shutting down the display and the hard disk after periods of inactivity. A user sometimes runs UNIX programs in text mode, and at other times uses the X Window System. She is surprised to find that battery life is significantly better when she uses text-only programs. Why?

### Deliverables
Commit the answers to the questions in a readable file to your git repository by the due date and time indicated with your repository. Approved file submission formats are: .txt, .md, .pdf. .html (renderable) or anything that is web-readable on Github. Other formats will only be accepted with *explicit approval*.
