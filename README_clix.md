# ATtiny-Punk-Console clix ROM

Proposed function

One (or more, depends on max space on chip. if more the one is possible, then pseudorandomly chosen) Clix samples are played back and repeated after a delay. 

A base delay time is controled by pot1, delay range between 2 sec (sparse clix) and 30ms (alomost contiuous noise).

After each click a pseudo-natural random factor R=(rand(10)+Rand(10))/2-10 is generated, so ranging from -10...10, smaller absolute values are some more likely this way) to modify the base delay time for the next click.

dlyT =dlyB-dlyT*R*pot2/10  (pot2 weights the amout of this randomness from 0 to delay time vaies from 0 to 2 * base delaytime)

In clix play back, according to pot3 the sample values are taken for playback: every 2nd, 3rd ranging from normal playback to only one sample
Another random factor Q after each click controls randomness of this "pitch" by pot4
