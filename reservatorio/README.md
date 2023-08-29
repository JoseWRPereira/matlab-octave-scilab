# Resposta ao degrau em Reservatório de fluído

```m
%
% Reservatório
%

A=0.1;        % área [m²];
R=1000;       % Restrição da válvula de saída em [s/m²] sendo 1000 s/m² a abertura total;
Qe=1;         % Vazão na válvula de entrada em [l/s] sendo 1 l/s a vazão máxima;
K = R;        % Ganho estático
tau=R*A;      % Constante de tempo
y0 = 0;       % Nivel inicial do tanque em [m]

t=linspace(0,1000,1001);

figure(1)
hold on
              % Restrição da válvula: abertura total
y=y0+K*Qe*(1-e.^(-t/tau));
plot(t,y,'r');

              % Restrição da válvula: abertura em 50%
y=y0+(K/2)*Qe*(1-e.^(-t/tau));
plot(t,y,'b');

title("Resposta ao degrau");
xlabel("Tempo[s)");
ylabel("Altura y[m]");
```

[Resposta ao Degrau]()
