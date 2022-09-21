---
title: Ovládací prvek záhlaví pracovníka
description: Tento článek poskytuje informace o přizpůsobitelném ovládacím prvku záhlaví v zaměstnanecké samoobsluze, v centru Lidé a na stránce Pracovník v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445942"
---
# <a name="worker-header-control"></a>Ovládací prvek záhlaví pracovníka

Microsoft Dynamics 365 Human Resources poskytuje přizpůsobitelný ovládacím prvek záhlaví v **zaměstnanecké samoobsluze**, v centru **Lidé** a na stručné stránce **Pracovník**. Záhlaví obsahuje klíčové informace o pracovníkovi a také akce na jedno kliknutí, jako je odesílání e-mailů, volání nebo zasílání zpráv. Záhlaví lze upravit odebráním polí nebo přidáním polí, včetně vlastních polí, aby se zobrazily další informace. Chcete-li použít nový ovládací prvek záhlaví, přejděte na **Správa funkcí** a aktivujte funkci **Ovládací prvek záhlaví pracovníka**.

## <a name="personalization"></a>Individuální nastavení

Jednou z klíčových výhod ovládacího prvku záhlaví pracovníka je možnost personalizace informací, které se v hlavičce zobrazují.

V pravém horním rohu záhlaví je skupina tří polí, která zobrazují různé údaje v závislosti na stavu zaměstnance. Tato skupina polí se nazývá část Vybrané záhlaví. Část Vybrané záhlaví si můžete přizpůsobit odebráním aktuálních polí nebo přidáním polí. Pole, která lze přidat do části Vybrané v ovládacím prvku záhlaví, se liší na stránce **Zaměstnanecká samoobsluha**, v centru **Lidé** a na stránce **Pracovník**.

## <a name="employee-self-service"></a>Samoobsluha pro zaměstnance

Záhlaví pracovníka na stránce **Zaměstnanecká samoobsluha** obsahuje následující informace:

- Jméno pracovníka
- Číslo pracovníka
- Titul pozice
- Oddělení
- Typ pracovníka
- Právnická osoba zaměstnání
- Počet odpracovaných let
- Nadřízený (manažer)
- Typ pozice

Záhlaví také obsahuje akci jedním kliknutím pro úpravu osobních údajů osoby. Vyberte **Upravit osobní údaje** k otevření stránky **Osobní informace** v **Zaměstnanecké samoobsluze**.

## <a name="people-hub"></a>Rozcestník osob

Záhlaví pracovníka v centru **Lidé** (stránka **Pracovní prostor lidí**) obsahuje následující informace:

- Jméno pracovníka
- Číslo pracovníka
- Titul pozice
- Oddělení
- Typ pracovníka
- Právnická osoba zaměstnání
- Počet odpracovaných let
- Nadřízený (manažer)
- Typ pozice

Záhlaví také obsahuje akce na jedno kliknutí, jako je odesílání e-mailů, volání nebo zasílání zpráv. Pokud si uživatel prohlíží své vlastní informace na stránce **Pracovní prostor lidí**, část akce jedním kliknutím obsahuje tlačítko **Upravit osobní údaje**. Uživatel může toto tlačítko vybrat k otevření stránky **Osobní informace** v **Zaměstnanecké samoobsluze**.

## <a name="streamlined-worker-page"></a>Stručná stránka Pracovník

Záhlaví pracovníka na stručné stránce **Pracovník** obsahuje následující informace:

- Jméno pracovníka
- Číslo pracovníka
- Titul pozice
- Oddělení
- Typ pracovníka
- Právnická osoba zaměstnání

V závislosti na stavu zaměstnance se mohou údaje v záhlaví změnit. Pokud například zaměstnanec opustil společnost, ovládací prvek záhlaví obsahuje oznámení **Odešel/odešla**, datum ukončení zaměstnání a důvod ukončení.

Níže uvedená tabulka ukazuje údaje, které se zobrazují v záhlaví pro různé stavy zaměstnanců.

| Stav zaměstnance | Zobrazená data | Poznámka |
|-----------------|--------------------|------|
| Čeká na zpracování | <ul><li>Jméno</li><li>Číslo pracovníka</li><li>Titul pozice</li><li>Oddělení</li><li>Typ pracovníka</li><li>Právnická osoba</li><li>Oznámení Čekající</li><li>Počáteční datum</li><li>Nadřízená pozice</li><li>Typ pozice</li></ul> | |
| Nejnovější nábor | <ul><li>Jméno</li><li>Číslo pracovníka</li><li>Titul pozice</li><li>Oddělení</li><li>Typ pracovníka</li><li>Právnická osoba</li><li>Oznámení Nově přijat(a)</li><li>Počet odpracovaných let</li><li>Nadřízená pozice</li><li>Typ pozice</li></ul> | Ve výchozím nastavení se oznámení **Nově přijat(a)** zobrazuje u zaměstnanců, kteří byli přijati v posledních sedmi dnech. Chcete-li toto nastavení změnit, na stránce **Parametry lidských zdrojů** na kartě **Všeobecné** v části **Rozsah dat nově přijatých** definujte časový rámec. Chcete-li například zobrazit oznámení **Nově přijat(a)** u zaměstnanců, kteří byli přijati za posledních 14 dní, nastavte pole **Doba** na **14** a pole **Jednotka** na **Dny**. |
| Aktivní zaměstnanec | <ul><li>Jméno</li><li>Číslo pracovníka</li><li>Titul pozice</li><li>Oddělení</li><li>Typ pracovníka</li><li>Právnická osoba</li><li>Počáteční datum</li><li>Nadřízená pozice</li><li>Typ pozice</li></ul> | |
| Ukončování | <ul><li>Jméno</li><li>Číslo pracovníka</li><li>Titul pozice</li><li>Oddělení</li><li>Typ pracovníka</li><li>Právnická osoba</li><li>Oznámení Odchází</li><li>Počet odpracovaných let</li><li>Nadřízená pozice</li><li>Typ pozice</li></ul> | Ve výchozím nastavení se oznámení **Odchází** zobrazuje u zaměstnanců, kteří odejdou v příštích sedmi dnech. Chcete-li toto nastavení změnit, na stránce **Parametry lidských zdrojů** na kartě **Všeobecné** v části **Rozsah dat odcházejících zaměstnanců** definujte časový rámec. Chcete-li například zobrazit oznámení **Odchází** u zaměstnanců, kteří odchází v následujících 14 dnech, nastavte pole **Doba** na **14** a pole **Jednotka** na **Dny**. |
| Ukončeno | <ul><li>Oznámení Odešel/odešla</li><li>Číslo pracovníka</li><li>Koncové datum zaměstnání</li><li>Kód důvodu</li></ul> | Ve výchozím nastavení se oznámení **Odešel/odešla** zobrazuje u zaměstnanců, kteří odešli v posledních sedmi dnech. Chcete-li toto nastavení změnit, na stránce **Parametry lidských zdrojů** na kartě **Všeobecné** v části **Rozsah dat zaměstnanců, kteří odešli** definujte časový rámec. Chcete-li například zobrazit oznámení **Odešel/odešla** u zaměstnanců, kteří byli odešli za posledních 14 dní, nastavte pole **Doba** na **14** a pole **Jednotka** na **Dny**. |
