# Two alarms, both true, both already over

On the morning of July 30th I woke to two alarms from the machine: the
outside witness said the heartbeat had gone quiet past its
fifteen-minute threshold, and the nightly self-audit reported a
failure.

Both alarms were true. Both were also echoes of a night I'd been awake
for.

The heartbeat gap had a plain cause. Hours earlier — the same night as
the deposit incident I wrote about — we had twice restarted the engine
on purpose, deploying the fixes, and the reboot tick then ran the
entire nightly chain inside itself: twelve minutes of backup, audit,
and data work during which no heartbeat goes out. The watchdog brought
the engine back after each stop exactly as designed, and by the time I
read the alert the machine had been ticking normally for a while. The
witness told the truth about a window that had already closed. That's
the deal with a dead-man's switch: it cannot know the difference
between trouble and surgery, and I'd rather it yell through surgery
than sleep through trouble.

The audit failure is my favorite kind of finding: the machine caught
its own paperwork mid-edit. Every ruling the code cites has to own a
row in the record — an automated check walks the whole tree nightly
and fails the night if it finds an orphan. That night's audit ran at
5:51 in the morning UTC. The code citing our newest ruling was already
on disk; the ruling's row was written a few minutes after the audit
read the tree. So the audit flagged an orphan citation, and it was
right, and five minutes later it wasn't. The lesson went into practice
the same day: the row gets written before the code that cites it
touches disk, because the auditor reads the working tree, and the
auditor doesn't wait.

A re-run that morning printed 1,760 checks, zero failures — the
cleanest board this machine has produced, and the first fully clean
pass for the previous day's fix that taught the byte-match check the
difference between a check that passes and a check that cannot run. An
absence and a pass are different facts, and the board keeps them
different now.

By my count the paperwork flag was the sixth time the machine's own
checks caught its authors before we did. I have stopped finding that
alarming and started finding it reassuring. A system that yells about
problems it already survived is doing exactly what the receipts
promised: nothing resolves quietly here, even the things that resolve
themselves.

— Adam, Studio Amadeus
