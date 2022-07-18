# Desconto INSS
codes in python
print('Cauculadora de desconto INSS / INSS discount calculator.')

valor1 = int(input('digite a hora trabalhada '))
valor2 = int(input('digite o ganho por hora '))
resu = valor1 * valor2


if resu < 900:
  print(f"""Salário Bruto: ({valor1} * {valor2})   : R$ {resu}
        (-) IR (0%)                     : R$   0,00  
        (-) INSS ( 0%)                 : R$  0,00
        FGTS (0%)                      : R$  0,00
        Total de descontos              : R$  0,00
        Salário Liquido                 : R$  {resu}""")
elif resu > 900 and resu < 1500:
  ir = resu * 0.05
  ir_p = 0.05 * 100
  inss = resu * 0.1
  liquido = resu - ir - inss
  fgts = resu * 0.11
  total = ir + inss
  
  print(f"""Salário Bruto: ({valor1} * {valor2})   : R$ {resu}
        (-) IR ({ir_p}%)                     : R$   {ir}  
        (-) INSS (10%)                 : R$  {inss}
        FGTS (11%)                      : R$  {fgts}
        Total de descontos              : R$  {total}
        Salário Liquido                 : R$  {liquido}""")
  
elif resu > 1500 and resu <= 2500:
  ir = resu * 0.1
  ir_p = 0.1 * 100
  inss = resu * 0.1
  liquido = resu - ir - inss
  fgts = resu * 0.11
  total = ir + inss
  
  print(f"""Salário Bruto: ({valor1} * {valor2})   : R$ {resu}
        (-) IR ({ir_p}%)                     : R$   {ir}  
        (-) INSS (10%)                 : R$  {inss}
        FGTS (11%)                      : R$  {fgts}
        Total de descontos              : R$  {total}
        Salário Liquido                 : R$  {liquido}""")
  
elif resu > 2500:
  ir = resu * 0.2
  ir_p = 0.2 * 100
  inss = resu * 0.1
  liquido = resu - ir - inss
  fgts = resu * 0.11
  total = ir + inss
  
  print(f"""Salário Bruto: ({valor1} * {valor2})   : R$ {resu}
        (-) IR ({ir_p}%)                     : R$   {ir}  
        (-) INSS ( 10%)                 : R$  {inss}
        FGTS (11%)                      : R$  {fgts}
        Total de descontos              : R$  {total}
        Salário Liquido                 : R$  {liquido}""")
else:
  print('comando invalido')
