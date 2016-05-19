# DSP
*MATLAB functions for digital signal processing made easy*

* dBbandProportion
   * p = dBbandProportion(CSC,loF,hiF,*'property'*,*value*)
   
   Returns the proportion of the area under the total spectral density curve that is within a frequency band between loF and hiF of a 
   continuously-sampled time-stamped signal CSC.
   
* ez_psd
   * ez_psd(csc)
    where           csc         is a continuously-sampled channel tsd
   will plot the power-spectral density (dB/Hz vs Hz) function.
   psdObj = ez_psd(csc)
    where           csc             is a continuously-sampled channel tsd
                    psdObj          is a structure with fields
                           .freq     is a vector of frequencies
                           .data     is the power spectral density
                          .fs       is the sampling frequency
                          .fnyquist is the nyquist frequency (Fs/2)
                          .dt       is the time difference of the original csc
                          .dF       is the frequency difference of the power spectral density function
                          .NFFT     is the number of discrete points used for the fast Fourier transform
* ez_spectrum
   * [Spectrum,RawFFT] = ez_spectrum(signal)
   
   Returns spectral components of signal
   
* LoadCSC_Header
   * Header = LoadCSC_Header(filename)
   
   Returns header information from Neuralynx continuously-sampled channel .ncs file filename.
   
* ma_psd
   * psdObj = ma_psd(csc,window)
   
   Returns a psdObj that has been smoothed with a moving average of size window.
   
* window_smoothing
   * yy = window_smoothing(y,smoothingWindow)
   
   Returns a signal that has been smoothed with a moving average of size smoothingWindow
