---
title: Přehled indické daně odečtené u zdroje (TDS)
description: Toto téma poskytuje podrobné informace o indické dani odečtené u zdroje (TDS). Dokumentace TDS pokrývá funkčnost této funkce.
author: kailiang
ms.date: 03/19/2021
ms.topic: overview
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d33faaff8be4821005b8772875eb91f0afe26cb0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983896"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Přehled indické daně odečtené u zdroje (TDS)

[!include [banner](../includes/banner.md)]

Toto téma poskytuje podrobné informace o indické dani odečtené u zdroje (TDS).

Dokumentace TDS pokrývá funkčnost této funkce. Vysvětluje také, jak provést základní nastavení pro TDS, vypočítat TDS u transakcí, provést proces vypořádání TDS, zaznamenat čísla certifikátů TDS a generovat dotazy TDS, příkazy TDS a certifikáty TDS. Dokumentace obsahuje následující témata:

- [Základní nastavení pro TDS](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Návrhář vzorců a funkce mezního limitu použitá pro výpočet TDS](apac-ind-TDS-Formula-designer.md)
- [Výpočet TDS na faktury, platby, směnky a mezipodnikové transakce](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Pravidelný proces vypořádání TDS a vypořádání částek TDS k dodavatelů autorit TDS](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [Záznam a aktualizace čísel a dat certifikátu TDS](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Úvod do TDS

Podle zákona o dani z příjmu z roku 1961 je daň z příjmu odebírána u zdroje příjemcem služby v době zálohy nebo zúčtování kreditu, podle toho, co nastane dříve. Osoba, která provádí platbu, musí odečíst částku daně a zaplatit pouze čistý zůstatek poskytovateli služby. TDS se aplikuje na služby, které stanoví vláda, a daň se odečte za použití sazeb stanovených vládou pro určité období. Míra odpočtu je založena na stavu subjektu, který přijímá platbu nebo poskytuje službu. Stavy zahrnují **Osoba**, **Hinduistická nerozdělená rodina** (**HUF**), **Společnost**, **Firma**, **Sdružení osob** (**AOP**), **Organizace jednotlivců** (**BOI**) a **Obecní úřad**.

V následujících částech je uveden seznam služeb, na které se TDS aplikuje, jak stanoví vláda Indie.

**Obyvatelé**

- Příjmy z platů (pod §192)
- Příjem z úroků z cenných papírů (podle §193)
- Příjmy z dividend (podle §194)
- Příjmy z úroků (podle §194A)
- Příjmy z loterií nebo soutěží (podle §194B)
- Vítězství na dostizích atd. (Podle § 194BB)
- Dodavatelé a subdodavatelé (podle §194C)
- Pojistná provize (podle §194D)
- Příjem z vkladu v rámci národního systému spoření (podle §194EE)
- Příjem ze podílového fondu nebo UTI (podle §194F)
- Provize, odměna, cena atd. za prodej nebo loterii (podle §194G)
- Výplata provize nebo zprostředkování (podle §194H)
- Nájemné (podle §194I)
- Profesionální služby (podle §194J)
- Příjmy z jednotek (podle §194K)
- Výplata kompenzace při nabytí určitého nemovitého majetku (podle §194LA)

**Nerezidenti**

- Platby nerezidentním sportovcům nebo sportovním svazům (podle §194E)
- Ostatní částky (podle §195)
- Příjmy za jednotky nerezidentů (podle §196A)

    - Výnosy z dluhopisů nebo akcií indické společnosti v cizí měně (podle §196C)
    - Příjmy zahraničních institucionálních investorů z cenných papírů (podle §196D)
    - Plat a všechny ostatní kladné příjmy podle jakéhokoli paragrafu o příjmu (§192)
    - Úroky z cenných papírů (§193)
    - Úroky jiné než úroky z cenných papírů (§194A)
    - Platby dodavatelům a subdodavatelům (§194C)
    - Výhry z loterie nebo křížovek (§194B)
    - Výhry z dostihů atd. (§194BB)
    - Pojišťovací provize pokrývající všechny platby za pojišťovací činnost (§194D)
    - Jakýkoli jiný úrok než úrok z cenných papírů splatný nerezidentům, kteří nejsou společností, nebo zahraniční společnosti (§195)
    - Platba nerezidentnímu sportovci včetně sportovce nebo sportovního svazu nebo instituce. V případě nerezidentního sportovce platby v souvislosti s reklamami a články o jakékoli hře/sportu v Indii v novinách, časopisech atd. jsou zahrnuty (§194E)
    - Platba za vklady v rámci NSS \[Národní systém spoření\] (§194EE)
    - Platba na účet zpětného odkupu podílových listů podílovým fondem nebo UTI (§194F)
    - Výplata provize nebo zprostředkování (§194H)
    - Platba nájemného (§194I)
    - Úhrada poplatků za odborné nebo technické služby (§194J)
    - Provize prodejcům, distributorům, kupujícím a prodejcům loterijních tiketů, včetně odměn nebo výher za tyto tikety (§194G)
    - Výnosy z podílových listů nakoupených v cizí měně nebo dlouhodobý kapitálový zisk z převodu těchto podílových jednotek nakoupených v cizí měně (§196B)
    - Výplata jakýchkoli příjmů nerezidentům z úroků nebo dividend z dluhopisů a akcií (§196C)

TDS se počítá za nákupy, prodeje, výnosy z prodeje, dobropisy, akvizice dlouhodobého majetku, zálohy, zálohy, směnky, daň z prací a mezipodnikové transakce.

> [!NOTE]
> V aktuálním indickém daňovém scénáři se TDS nevypočítává z prodejních transakcí. Systém však zahrnuje rezervu na výpočet TDS zpětně získatelných u prodejních transakcí, zejména u transakcí mezi společnostmi.

Výpočet TDS vždy zohledňuje prahovou hodnotu a prahovou hodnotu výjimky, které jsou definovány pro komponentu TDS.

Musí být spuštěn pravidelný proces vypořádání TDS a platby TDS musí být vypořádány prodejcům autorit TDS.

Je možné zaznamenávat a aktualizovat čísla a data certifikátů TDS, která jsou přijímána od prodejců nebo zákazníků. Navíc lze ve Finance generovat čtvrtletní výkazy formuláře 26Q a formuláře 27Q a certifikát formuláře 16A pro TDS.

## <a name="setting-up-and-working-with-tds"></a>Nastavení a práce s TDS

Zde je přehled procesu nastavení a práce s TDS:

1. **Nastavení TDS:**

    - Nastavení parametrů:

        - V parametrech hlavní knihy aktivujte parametry související s TDS.
        - V parametrech hlavní knihy nastavte číselnou řadu pro platby srážkové daně.
        - Nastavte parametry v závazcích a pohledávkách.

    - Základní nastavení:

        - Nastavte registrační čísla TDS pro společnost, zákazníky a dodavatele.
        - Nastavení skupin komponent TDS.
        - Nastavte komponenty TDS, připojte k nim skupiny komponent TDS a definujte pro ně prahovou hodnotu a prahovou hodnotu výjimky.
        - Nastavte oprávnění TDS.
        - Nastavte období vyrovnání TDS.
        - Nastavte daňové kódy TDS a připojte k nim komponenty TDS.
        - Nastavte daňové skupiny TDS a připojte k nim daňové kódy TDS.
        - V návrháři vzorců definujte vzorec pro výpočet TDS pro skupinu TDS.
        - Zaznamenejte čísla koncesních certifikátů TDS.

    - Účty hlavní knihy a nastavení společnosti:

        - Nastavte účty hlavní knihy pohledávky a zakázky.
        - Nastavte pro společnost daňový odpočet a číslo účtu inkasa (TAN) a kategorii typu odpočtu.

    - Další nastavení:

        - Nastavte plán plateb, který zahrnuje přidělení TDS.
        - Nastavte typ platebního poplatku pro platby úřadu TCS.
        - Nastavte informace o skupinách TDS, stálých číslech účtů (PAN) a TAN pro dodavatele a zákazníky.

2. **Výpočet TDS v transakcích:**

    - Faktury a platby
    - Vlastní směnky
    - Platby předem
    - Zálohy

3. **Vyrovnání TDS:**

    - Periodický proces vypořádání TDS
    - Vypořádání plateb TDS prodejcům autorit TDS a generování challan TDS

4. **Dotazy, výkazy a certifikát TDS:**

    - Zaznamenejte a aktualizujte čísla a data certifikátu TDS.
    - Vygenerujte dotaz TDS a zaúčtovaný dotaz TDS.
    - Generujte čtvrtletní výkazy Formuláře 27A, Formuláře 26Q a Formuláře 27Q TDS a e-TDS.
    - Vygenerujte certifikát TDS formuláře 16A.
