# Yin

Mirror of the YIN matlab library matlab by Alain de Cheveigné, redistributed
uner the terms of the original [licence](./LICENCE).

The point of entry is the `yin` function which calls on other functions using
the [`private/` directory sturcture of
MATLAB](https://www.mathworks.com/help/matlab/matlab_prog/private-functions.html).

Yin uses c source files using the
[MEX](https://www.mathworks.com/help/matlab/ref/mex.html) compilation system.
Setup is partially covered in the original [`INSTALL`](./INSTALL) file. In
addition there is a [`setupyin.m`](./setupyin.m) script which has been added to make things a
little easier.

## Original Documentation

>[!NOTE] 
>The original README was more of a licence, which has been moved to [`./LICENCE`](./LICENCE).
>
>Below is a copy of the original `.html`,  added here for ease.


>### YIN: fundamental frequency estimator
>
>YIN estimates the fundamental frequency (F0) of an audio signal. Features are:
>
>-   Reliability (based on tests, see reference below).
>-   Accuracy (subsample resolution).
>-   Wide search range (default is 30 Hz - sr/4).
>-   Good temporal resolution.
>-   Ease of use.
>
>YIN operates on vectors or files. YIN outputs a structure containing a set of
>four vectors: F0 vs time, two estimates of aperiodic/total power (one gross
>estimate, one fine estimate), and a period-smoothed estimate of instantaneous
>power.
>
>If no output argment is specified, YIN plots F0 as a function of time (in
>octaves re: 440 Hz), aperiodicity, and power.
>
>In the F0 plot, samples in blue are reckoned reliable
>(aperiodicity2\*threshold).
>
>Type 'help yin' for a description of the parameters. Read the reference below
>and the code to understand their meaning. In brief:
>
>-   To increase speed: increase 'hop' or 'minf0'.
>-   To reduce memory needs: reduce 'bufsize', or increase 'hop' or 'minf0'.
>-   To slightly increase reliability: reduce 'hop'.
>-   To slightly increase precision: upsample before processing.
>-   To improve temporal resolution: increase 'minf0', decrease 'hop'.
>-   To process lower F0s: reduce 'minf0'. Higher F0s: upsample and increase
>    'maxf0'.
>-   To avoid subharmonic errors: increase 'thresh'.
>-   To avoid harmonic/formant errors: reduce 'thresh'.
>-   Make sure that the range \[minf0 maxf0\] includes the expected f0.
>
>Parameter 'thresh' sets the proportion of aperiodic power that is tolerated
>within a "periodic" signal. This may vary according to the application.
>
>For speech or musical instruments a value of 0.1 is usually adequate. Singing
>voice may require a smaller value (as low as 0.001) if a harmonic is reinforced
>by a sharp formant.
>
>Some signals are inherently ambiguous. For example the response of a high-Q
>resonator excited by a pulse train may be seen either as a complex tone with an
>F0 equal to that of the pulse train, or as an amplitude modulated pure tone with
>an F0 equal to the resonant frequency. Neither is more "correct" than the other.
>To obtain the result that you expect, you must set the threshold to an
>appropriate value: small for the fundamental periodicity, large for the
>resonance periodicity.
>
>YIN is described in: de Cheveigné, A., and Kawahara, H. (2002). "YIN, a
>fundamental frequency estimator for speech and music," J. Acoust. Soc. Am., 111,
>1917-1930. ([pdf](http://www.ircam.fr/pcm/cheveign/ps/yin.pdf))

------------------------------------------------------------------------
## Links

- [Original `.zip` link](http://www.ircam.fr/pcm/cheveign/sw/yin.zip)[404: but this linked to
the source code in this repository]

- [Alain de Cheveigné](http://www.ircam.fr/pcm/cheveign)[404
[Wayback](https://web.archive.org/web/20020827085543/http://www.ircam.fr/pcm/cheveign/)]
