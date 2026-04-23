# CECS 326 Study Questions: Input and Output

Ten tiered review questions covering all three sessions of the I/O unit.
Work with one or two partners if you want, but all students submit individually.

## Recall (2 questions)

**Q1.** `[Recall]` State the four properties of a precise interrupt. For each,
explain in one sentence why violating it would make interrupt handlers harder
to debug or restart.

**Q2.** `[Recall]` Name the four layers of the classical I/O software stack from
lowest to highest. For each layer, state one responsibility that does NOT belong
in any of the other three.

## Apply (3 questions)

**Q3.** `[Apply]` Given the disk request queue {10, 22, 20, 2, 40, 6, 38} with
the arm initially at cylinder 20 and a seek cost of 6 ms per cylinder, compute
the total seek time for (a) FCFS, (b) Shortest Seek First, (c) the Elevator
algorithm initially moving upward. Show your work.

**Q4.** `[Apply]` A DMA controller has five channels. Each channel requests a
32-bit word every 40 ns, and a response takes equally long. Compute the minimum
bus bandwidth in MB/s. Then explain in one sentence why this question is almost
meaningless on a 2026 system.

**Q5.** `[Apply]` A CECS 326 student runs the same small program on two laptops.
Laptop A has a 7200 RPM SATA HDD; Laptop B has a PCIe Gen4 NVMe SSD. The program
issues 10,000 random 4 KB reads. Estimate the elapsed time on each laptop and
explain which component of disk access (seek / rotation / transfer) dominates
on each.

## Analyze (5 questions)

**Q6.** `[Analyze]` The July 2024 CrowdStrike Falcon outage was caused by a
null-pointer dereference in a kernel-mode driver reading a malformed channel
file. Using the four-layer I/O software model, identify which layer(s) the bug
lived in, and discuss whether a user-mode driver framework (Windows UMDF,
macOS DriverKit) would have prevented the outage. What would moving Falcon to
user mode have cost?

**Q7.** `[Analyze]` Reading Q5 asks what happens if a manufacturer redesigns the
MBR partition table to allow more than four partitions. Answer the question,
then extend it: explain why the industry eventually adopted GPT instead of
extending MBR, and what GPT gave up in exchange. Your answer should reference
at least one concrete 2026 system that still requires MBR for compatibility.

**Q8.** `[Analyze]` Elevator disk scheduling was designed to minimize arm motion
on spinning media. For modern NVMe SSDs the default Linux scheduler is `none`.
Defend or refute the following claim: "Disk arm scheduling algorithms are a
purely historical topic in 2026 and should be removed from the CECS 326
curriculum." Your answer should name at least one scenario where reordering is
still useful even in the absence of seek cost.

**Q9.** `[Analyze]` `io_uring` gives 2–10× throughput improvement for I/O-dense
workloads by replacing per-operation syscalls with a shared ring buffer. In
2023 it was also the origin of the majority of Linux kernel exploits. Evaluate
the tradeoff: for which applications is `io_uring` worth enabling, and which
applications should leave it off? Use the six I/O software goals from Session 1
to structure your answer.

**Q10.** `[Analyze]` Reading Q10 explains why a laptop's battery lasts longer
in text mode than under X Windows. Rewrite the answer for a 2026 laptop with an
OLED display, an NVMe SSD, a modern ARM or x86 CPU with fine-grained idle
states, and a modern wayland compositor. Which hardware still dominates the
power budget? Which factors from the original 2013-era answer no longer apply?

### Collaboration

You may work with one or two partners but all students must submit individually.

### Deliverables
* Your writeup file *must* be done in [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) format and must be included in the repository as a separate file. View the file [`README.md`](README.md?plain=1) for an example of Markdown.
* Any included images or screenshots should be done in `*.jpg`, `*.png`, or `*.gif` formats, and be included individually as files in your repository (i.e. no binary ‘document’ with the images pasted inside).
* Screenshots or images *may* be linked in your Markdown file writeup if you wish to do so.
