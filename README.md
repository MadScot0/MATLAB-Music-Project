 %MELODY
 
 Fs=8000;        % Assign a sample frequency of 8000.
 Ts=1/Fs;
 t=[0:Ts:0.35];  % Assign the duration of each notes as 0.35 seconds.
 C = 262; D = 294; E = 330; F = 349; G = 392; A = 440; B = 494; C_High = 523; rest = 5000000;
 notes = [E; E; F; G; G; F; E; D; C; C; D; E; E; D; D; rest; E; E; F; G; G; F; E; D; C; C; D; E; D; C; C; rest];
 x = sin(2*pi*notes*t);
 melody1 = reshape(x',32*length(t),1); 
 sound(melody1, Fs)
 
 %ACCOMPANIMENT
 
 Fs=8000;        % Assign a sample frequency of 8000.
 Ts=1/Fs;
 t=[0:Ts:5.6];   % Assign the duration of each notes as 0.35 seconds.
 C = 262; D = 294; E = 330; F = 349; G = 392; A = 440; B = 494; C_High = 523; G_Low = 98; rest = 5000000;
 notes = [C;C]
 x = sin(2*pi*notes*t);
 melody2 = reshape(x',2*length(t),1); 
 sound(melody2, Fs)
