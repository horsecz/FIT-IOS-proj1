# IOS - projekt 1

- Projekt 1 do predmetu IOS - shell skript 'dirgraph' -> analyzuje a zjisti pocet souboru a slozek v danem adresari a vykresli histogram velikostí souboru.
- V ramci projektu byl vytvoren i skript 'dirgtest' (neni soucasti zadani projektu) za ucelem otestovani spravne funkce skriptu dirgraph.

# Hodnoceni
- 1/15 -> 12/15

# Poznamka
- Ve skriptu byly chyby, ktere zpusobily poprve dost nehezke hodnoceni, proto jsem vypracoval patch, ktery opravoval nasledujici chyby:
  - nekompatibilita: IFS=$'\n' zmeneno na IFS=" " (= enter -> \n -> newline)
  - spatny histogram: ve skriptu bylo -le (<=) misto -lt (<)
  - chybny vystup do souboru: smazany prubezne printf "\r .." u All files, ktere zpusobovaly rozbiti vypisu pri stdout=soubor
