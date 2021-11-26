---
title: Pracovní prostor správy personálu
description: Toto téma popisuje koncepční prvky pracovního prostoru správy personálu.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4332be972ab3dc81e7e4f3cc297a91cd247e721e
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771331"
---
# <a name="personnel-management-workspace"></a>Pracovní prostor správy personálu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pracovní prostor **Správa personálu** obsahuje obrovské množství obsahu. Obsahuje pohyby personálu, sleduje změny zaměstnanců, otevřené pozice, změny adres, expirační záznamy a analytiku a poskytuje odkazy na konkrétní informace. Toto téma obsahuje podrobné informace o každé části pracovního prostoru.

## <a name="activity-tab"></a>Karta Aktivita

Karta **Aktivita** obsahuje sekce, které seskupují pracovníky na základě jejich stadia v procesu zaměstnávání:

- **Kandidáti k přijetí**
- **Začne brzy**
- **Nejnovější přijetí**
- **Ukončování**
- **Ukončeno**

Když je pracovník v jedné z těchto fází, jsou konkrétní akce k dispozici jako tlačítko na kartě nebo v nabídce, která se zobrazí, když vyberete tři tečky (**…**) v pravém horním rohu. Následující pododdíly popisují oddíly karty **Aktivita** a seznam akcí, které jsou k dispozici.

### <a name="candidates-to-hire"></a>Kandidáti k přijetí

Část **Uchazeči o zaměstnání** pracovního prostoru je vyplněna z více zdrojů:

- Entita Open Data Protocol (OData)
- Integrace se službou LinkedIn
- Data, která se do produktu zadávají ručně

Když se kandidáti objeví v části **Uchazeči o zaměstnání**, můžete provést následující akce výběrem tří teček na kartě kandidáta:

- **Zamítnout kandidáta**
- **Nepřijímat**
- **Přijmout**

> [!NOTE]
> Pokud se seznam kandidátů vyplňuje z Microsoft Dataverse, budou se u všech právnických osob zobrazovat stejní kandidáti, protože ke kandidátovi nebyla přidružena žádná právnická osoba.

### <a name="starting-soon"></a>Začne brzy

Část **Brzy začíná** obsahuje pracovníky, kteří mají datum zahájení v budoucnu. Seznam je roztříděn podle počátečního data. Datum zahájení, které je nejblíže dnešním údajům, je uvedeno jako první.

Pokud se manažer na kartě neobjeví, nebyla pracovníkovi přiřazena pozice.

> [!NOTE] 
> Než použijete kontrolní seznam, doporučujeme přiřadit pozici pracovníkovi. Někdy jsou úkoly při nástupu přiděleny manažerovi nově přijatého zaměstnance. Pokud však není přiřazena žádná pozice, manažera nového zaměstnance nelze určit. V takovém případě budou úkoly přihlašování, které jsou určeny pro správce, přiřazeny vlastníkovi kontrolního seznamu.

Když se pracovníci objeví v části **Brzy začíná**, jsou pro ně k dispozici následující akce:

- Přiřadit pozici
- Ověřit zaměstnání
- Přiřadit fixní kompenzaci
- Přiřadit variabilní kompenzaci
- Zobrazit v hierarchii
- Použít kontrolní seznam\*\*

\*\* Tato akce je výchozí akce. Zobrazí se jako tlačítko na kartě.

### <a name="recent-hires"></a>Nejnovější přijetí

Část **Poslední přijatí** obsahuje pracovníky, kteří mají počáteční datum v nedávné minulosti. Seznam je roztříděn podle počátečního data. Datum zahájení, které je nejblíže dnešnímu datu, je uvedeno jako první.

Ve výchozím nastavení seznam zobrazuje pracovníky, kteří byli najati za posledních sedm dní. Chcete-li toto nastavení změnit, na stránce **Parametry lidských zdrojů** karty **Všeobecné** definujte časový rámec pro **Poslední přijatí**. Údaje v části **Poslední přijatí** lze zobrazit pro konkrétní počet dní, měsíců nebo let. Chcete-li například zobrazit seznam pracovníků, kteří byli přijati za posledních 14 dní, nastavte pole **Doba** na **14** a pole **Jednotka** na **Dny**.

> [!NOTE]
> Nastavení na stránce **Parametry lidských zdrojů** se liší podle společnosti. Časový rámec, pro který si prohlížíte poslední přijaté, se proto může u jednotlivých společností lišit. Například ve společnosti USMF možná budete chtít zobrazit všechny nové zaměstnance z posledních sedmi dnů. Ve společnosti USSI ale budete chtít zobrazit všechny nové zaměstnance z posledních 14 dnů. V tomto případě otevřete stránku **Parametry lidských zdrojů** v každé společnosti a podle potřeby nastavit parametry.

Pokud se manažer na kartě neobjeví, nebyla pracovníkovi přiřazena pozice.

Když se pracovníci objeví v části **Poslední přijatí**, jsou pro ně k dispozici následující akce:

- Přiřadit pozici
- Ověřit zaměstnání
- Fixní kompenzace
- Přiřadit variabilní kompenzaci
- Zobrazit v hierarchii
- Použít kontrolní seznam\*\*

\*\* Tato akce je výchozí akce. Zobrazí se jako tlačítko na kartě.

### <a name="exiting"></a>Ukončování

Část **Končí** obsahuje pracovníky, kteří mají datum ukončení v budoucnu. Seznam je roztříděn podle data ukončení. Datum ukončení, které je nejblíže dnešnímu datu, je uvedeno jako první. 

Ve výchozím nastavení seznam zobrazuje pracovníky, kteří mají datum ukončení v příštích sedmi dnech. Chcete-li toto nastavení změnit, na stránce **Parametry lidských zdrojů** karty **Všeobecné** definujte časový rámec pro **Zobrazit stávající pracovníky**. Údaje v části **Končí** lze zobrazit pro konkrétní počet dní, měsíců nebo let. Chcete-li například zobrazit seznam pracovníků, kteří skončí v následujících 14 dnech, nastavte pole **Doba** na **14** a pole **Jednotka** na **Dny**.

Když se pracovníci objeví v části **Končí**, jsou pro ně k dispozici následující akce:

- Použít kontrolní seznam\*\*
- Ověřit zaměstnání
- Zobrazit v hierarchii

\*\* Tato akce je výchozí akce. Zobrazí se jako tlačítko na kartě.

### <a name="exited"></a>Ukončeno

Část **Skončili** obsahuje pracovníky, kteří mají datum ukončení v nedávné minulosti. Seznam je roztříděn podle data ukončení. Datum ukončení, které je nejblíže dnešnímu datu, je uvedeno jako první.

Ve výchozím nastavení seznam zobrazuje pracovníky, kteří mají datum ukončení v posledních sedmi dnech. Chcete-li toto nastavení změnit, na stránce **Parametry lidských zdrojů** karty **Všeobecné** definujte časový rámec pro **Zobrazit pracovníky, kteří skončili**. Údaje v části **Skončili** lze zobrazit pro konkrétní počet dní, měsíců nebo let. Chcete-li například zobrazit seznam pracovníků, kteří skončili za posledních 14 dní, nastavte pole **Doba** na **14** a pole **Jednotka** na **Dny**.

Když se pracovník objeví v části **Skončili**, jsou pro něj k dispozici následující akce:

- Použít kontrolní seznam\*\*
- Ověřit zaměstnání
- Zobrazit v hierarchii

\*\* Tato akce je výchozí akce. Zobrazí se jako tlačítko na kartě.

## <a name="employee-changes-tab"></a>Karta Změny zaměstnanců

Karta **Změny zaměstnanců** poskytuje seznam všech akcí zaměstnanců. Tento seznam není k dispozici ve výchozím nastavení. Chcete-li povolit tuto funkci, na stránce **Sdílené parametry lidských zdrojů** na kartě **Akce zaměstnanců** nastavte možnost **Povolit akce pracovníka** na **Ano**.

## <a name="position-changes-tab"></a>Karta Změny pozice

Karta **Změny pozice** poskytuje seznam všech akcí zaměstnanců týkajících se pozice. Tento seznam není k dispozici ve výchozím nastavení. Chcete-li povolit tuto funkci, na stránce **Sdílené parametry lidských zdrojů** na kartě **Akce zaměstnanců** nastavte možnost **Povolit akce pozice** na **Ano**.

## <a name="open-positions-tab"></a>Karta Otevřené pozice

Karta **Otevřené pozice** obsahuje seznam všech otevřených pozic. Aby se pozice mohly zobrazit v seznamu, musí mít datum aktivace dnes nebo dříve a nesmí mít aktuální přiřazení pracovníka.

> [!NOTE]
> Seznam zobrazuje přiřazení pracovníka k dnešnímu dni. Jakákoli pozice, která má přiřazení pracovníka s datem v budoucnu, se bude v seznamu nadále zobrazovat. Po dosažení data účinnosti přiřazení pracovníka však bude pozice ze seznamu odstraněna.

## <a name="expiring-records-tab"></a>Karta Vyprší platnost záznamů

Karta **Platnost záznamů vyprší** obsahuje seznam všech položek, jejichž platnost vypršela nebo vyprší pro pracovníky ve společnosti, ke které je uživatel přihlášen. V seznamu se zobrazují následující položky:

- **Certifikáty**
- **Identifikace**
- **Zkušební doba**
- **Prověřování**
- **Testy**

Chcete-li určit, zda seznam zobrazuje záznamy, jejichž platnost vypršela nebo vyprší, na stránce **Parametry lidských zdrojů** na kartě **Všeobecné** definujte časový rámec pro **Záznamy, jejichž platnost končí** nebo **Záznamy, jejichž platnost skončila**. Data na kartě **Záznamy, jejichž platnost končí** může být zobrazena pro konkrétní počet dní. Chcete-li například zobrazit seznam záznamů, jejichž platnost vyprší za následujících 14 dní, nastavte pole **Počet dní** na **14**.

> [!NOTE] 
> Pokud nastavíte časový rámec pro **Záznamy po konci platnosti** nebo **Záznamy, jejichž platnost končí** na **0** na stránce **Parametry lidských zdrojů**, na stránce se žádný z těchto záznamů nezobrazí.

## <a name="employees-tile"></a>Dlaždice Zaměstnanci

Dlaždice **Zaměstnanci** poskytuje počet všech zaměstnanců, kteří jsou zaměstnáni ve společnosti, ke které je uživatel aktuálně přihlášen. Když vyberete dlaždici **Zaměstnanci**, na nové stránce se zobrazí podrobnosti o zaměstnancích.

## <a name="contractors-tile"></a>Dlaždice Dodavatelé

Dlaždice **Dodavatelé** poskytuje počet všech dodavatelů, kteří jsou zaměstnáni ve společnosti, ke které je uživatel aktuálně přihlášen. Když vyberete dlaždici **Dodavatelé**, na nové stránce se zobrazí podrobnosti o dodavatelích.

## <a name="open-positions-tile"></a>Dlaždice Otevřené pozice

Dlaždice **Otevřené pozice** poskytuje počet všech otevřených pozic. Když vyberete dlaždici **Otevřené pozice**, na nové stránce se zobrazí podrobnosti o otevřených pozicích. Aby se pozice mohly zobrazit v seznamu, musí mít datum aktivace dnes nebo dříve a nesmí mít aktuální přiřazení pracovníka.

> [!NOTE]
> Dlaždice zobrazuje přiřazení pracovníka k dnešnímu dni. Jakákoli pozice, která má přiřazení pracovníka s datem v budoucnu, se bude v seznamu nadále zobrazovat. Po dosažení data účinnosti přiřazení pracovníka však bude pozice z počítání vyjmuta.

## <a name="approvals-tile"></a>Dlaždice Schválení

Dlaždice **Schválení** poskytuje počet všech položek pracovního toku, které čekají na schválení aktuálním uživatelem. Když vyberete dlaždici **Schválení**, nová stránka zobrazuje podrobnosti o položkách pracovního postupu, které vyžadují váš souhlas.

## <a name="address-changes-tile"></a>Dlaždice Změny adresy

Dlaždice **Změny adresy** poskytuje počet všech změn adres, ke kterým došlo během počtu dnů, který je uveden na stránce **Parametry lidských zdrojů**. Když vyberete dlaždici **Změny adresy**, na nové stránce se zobrazí podrobnosti o všech změnách adresy. V pravém horním rohu můžete vybrat **Zahrnout budoucí změny adresy** pro zobrazení změn adresy s budoucím datem.

Další informace o tom, jak zobrazit a spravovat změny adres, najdete v části [Zobrazení a správa změn adres](hr-personnel-view-address-changes.md).
