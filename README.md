# C128_U36_adapter
A new design of the megabit adapter for U36 in the C128

# The story began
I tried to recreate the original Megabit adapter for the U36 socket in the C128.
The information to this project I found on cmb8bit.com. You can find the PDFs and the ROM binfile in the <strong>cmb8bit.com</strong> directory.

<ul>
    <li> <a href="./cbm8bit.com/Megabit_internal_rom_manual.pdf"> Megabit internal ROM manual</a> </li>
    <li> <a href="./cbm8bit.com/MegaBit-faq-howtoo.pdf"> Megabit FAQ HowTo</a> </li>
    <li> <a href="./cbm8bit.com/megabit-help.BIN"> megabit-help.bin</a> </li>
</ul>

# The issue began
I designed a PCB with the information of the PDFs and tested the soldered PCB. <br>
Unfurtunately it does not work :( <br>
Thankfully a guy (Kinzi) from the great Forum64 helped me out by troubleshooting. <br>
I scoped the signals and figured out, that the transistor I used was to slow to trigger the D-FF. <br>
After that I tried logic gates - but this does not work either.
I figured out that there is a GLITCH on Pin12 of U3 <br>
<img src="./pics/GLITCH_U3.jpg" alt="GLITCH on U3 pin 12"> <br>
Kinzi mentioned that the /CS sigal from pin12 of U3 has to be synchronized with the 1MHz clock of the C128. <br>
So I poked around with this solution and that was the goal. <br>


