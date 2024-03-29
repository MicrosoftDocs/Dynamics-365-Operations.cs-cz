---
title: Konfigurace typů životních událostí
description: Microsoft Dynamics 365 Human Resources používá typy životní události k definování událostí, které aktualizují registraci zaměstnaneckých výhod.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df523dd4da11e24c7b601c8f34aef24ad6cb3b18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336908"
---
# <a name="configure-life-event-types"></a>Konfigurace typů životních událostí

Dynamics 365 Human Resources používá **Typy životní události** k definování událostí, které jsou platné k aktualizaci přihlášení zaměstnaneckých výhod, jako je svatba nebo narození dítěte. Každý ID typu životní události lze přidružit pouze k jednomu typu životní události. Vytvoříte-li například **ID životní události** nazvané **Změna adresy**, která je přidružená k typu životní události **Změna adresy zaměstnance**, nelze vytvořit další ID s názvem **Změna adresy zaměstnance** a spojit je s typem události **Změna adresy zaměstnance**. Pokud typ životní události není spojen s typem plánu, typ životní události nespustí životní událost. Další informace viz [Vytvoření typů plánů](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Vytvoření typu životní události

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **typy životní události**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **ID typu životních událostí** | Jedinečný identifikátor typu životní události. |
   | **Popis** | Popis typu životní události. |
   | **Typy životní události** | Katalyzátor pro aktualizaci přihlášení zaměstnaneckých výhod. Seznam životních událostí naleznete v tématu [Životní události](hr-benefits-setup-payment-frequencies.md?life-events) níže. |

4. Zvolte **Uložit**.

## <a name="view-attached-plans"></a>Zobrazit přiložené plány

Můžete zobrazit seznam plánů, které jsou připojeny k vybranému **typu životní události**. Události životního cyklu jsou připojeny k typu plánu a typy plánů jsou přidruženy k plánu.

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **typy životní události**.

2. Vyberte **Akce**.

3. Vyberte **připojené plány**.

## <a name="life-events"></a>Životní události

Při vytváření typu životní události můžete vybrat některou z následujících životních událostí:

| Životní událost | Umístění | Aktivační událost |
| --- | --- | --- |
| **Změna rodinného stavu** | **Pracovník> Profil > osobní údaje > Rodinný stav**| Změna v rodinném stavu |
| **Změna stavu zaměstnání** |**Pracovník > Zaměstnání > stránka Historie zaměstnance** | U pracovníka s existujícím podrobným údajem o zaměstnání vyvolá vytvoření nového pracovního detailu s jiným stavem zaměstnání životní událost.  Aktualizace stávajícího detailu zaměstnání s odlišným stavem zaměstnání také spustí životní událost.  |
| **Změna adresy zaměstnance** |**Pracovník > Profil > Adresy**</li><li>**Pracovník > Osobní údaje > Osobní kontaktní > Adresa**</li></ul> | Změna adresy. Ke spuštění životní události musí být adresa **Primární**. |
| **Změna rodinného příslušníka** |<br><ul><li>**Pracovník > Profil > Osobní údaje > Osobní kontakty**/li><li>**Samoobsluha pro zaměstnance**</li></ul> | Přidejte osobní kontakt, určete ho jako závislou osobu a definujte **Platnost od**. Aktualizujte údaj závislého osobního kontaktu **Platnost do**. Vztah osobního kontaktu musí být dítě, manžel/ka, druh/družka nebo bývalý manžel/manželka.  |
| **Narození nebo adopce (závislá osoba)** |<br><ul><li>**Pracovník > Profil > Osobní údaje > Osobní kontakty**</li><li>**Samoobsluha zaměstnanců > Upravit osobní údaje > Osobní kontakty**</li></ul>| Přidá se nebo aktualizuje **Datum narození** nebo **Datum adopce**. Je požadováno **Datum narození** dítěte. |
| **Ztráta pokrytí (manžel/ka nebo druh/družka)** | Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě> ztráta pokrytí | **Ztráta pokrytí** vybraná pro osobní kontakt spolu s **datem platnosti** |
| Změna zaměstnání druha/družky | **Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě >Zaměstnaná** | Vytvoření osobního kontaktu a nastavení **Zaměstnaná** na **Ano**. Aktualizace osobního kontaktu a změna hodnoty **Zaměstnaná**.  |
| **Pracovní volno (manžel/ka nebo druh/družka)** | **Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě> Pracovní volno** | Byl vytvořen osobní kontakt a je definováno **Datum účinnosti pracovního volna**. Je aktualizováno **Pracovní volno** osobního kontaktu. Je aktualizováno **Datum platnosti pracovního volna** osobního kontaktu.  |
| **Změna pokrytí (pozice)** |<br><ul><li>**Pracovník -> Přiřazení pozice > Přiřazení pozic pracovníka**</li><li>**Pozice > Pozice**</li></ul>| Změna na pozici v záznamech přiřazení pozice pracovníka. Změna přiřazení pracovníka na pozici. |
| **Změna pokrytí (mzda)** |<br><ul><li>**Pracovník > Kompenzace > Fixní plán**</li><li>**Pracovník > Osobní údaje > Roční plat zaměstnaneckých výhod**</li></ul>| Pokud není povolena možnost **Správa výhod > Sdílené parametry lidských zdrojů> Výhody> Roční plat výhod**, aktualizace údajů **Pracovník > Odměny > Pevný plán** vytvoří životní událost. Pokud je povolena možnost **Správa výhod > Sdílené parametry lidských zdrojů> Výhody> Roční plat výhod**, aktualizace údajů **Pracovník > Osobní informace > Roční plat zaměstnaneckých výhod** vytvoří životní událost. |
| **Zdravotní péče (zaměstnanec / závislá osoba)** | **Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě> Datum účinnosti zdravotní péče** | Přidávání nebo aktualizace data **Platnost Medicare** osobního kontaktu vytváří tuto životní událost. |
| **Soudně nařízená podpora** | **Pracovník > Profil > osobní údaje > Osobní kontakty > Závislá osoba > Podpora nařízená soudem** (QMSCO/QDRO) a data platnosti | Při vytváření osobního kontaktu bude vytvořena životní událost, pokud **Soud nařídil podporu** je **Ano**. Aktualizace **Soud nařídil podporu** nebo **Soudem nařízené datum vypršení platnosti** spustí také životní událost. |
| **Zemřel/a** | **Pracovník> Profil > osobní údaje > Datum úmrtí** | Je zadáno nebo aktualizováno **Datum úmrtí**. |
| **Důkaz pojištění** | **Pracovník > Pracovník > Verze > Historie zaměstnání > Kalendář > Správce dat > Podrobnosti o zaměstnanecké výhodě** | **Důkazy o pojistitelnosti** je nastaveno na **Ano**. Je definováno **Datum ověření důkazu o pojistitelnosti**. |
| **Příjemce** | **Pracovník > Profil > Osobní údaje > Osobní kontakty** | Je přidán osobní kontakt a jsou zadány hodnoty do polí **Příjemce** a **Datum účinnosti**. Osobní kontakt musí být typu **Dítě**, **Manžel/ka**, **DomesticPartner**, **Sourozenec**, **FamilyContact**, **OtherContact** nebo **Rodič**. |
| **Lékařská péče zaměstnance** | **Pracovník > Pracovník > Verze > Historie zaměstnání > Kalendář > Správce dat > Podrobnosti o zaměstnanecké výhodě** | **Nárok na Medicare** je nastaveno na **Ano**. **Datum nároku na Medicare** je změněno. |
| **Narozeniny** | **Správa výhod > Zpracování změn životních událostí** | Tyto životní události jsou vytvořeny z **Zpracování změn životních událostí**. Proces analyzuje zvolené období a právní subjekt a hledá přidružené pracovníky. Vypočítá jejich poslední narozeniny a vytvoří životní událost narozenin, pokud ještě nebyla vytvořena. |
| **Změna nároku pracovníka (netýká se USA)** |<br><ul><li>**Pracovník > Zaměstnání**</li><li>**Pracovník > pracovník > verze > Historie zaměstnání**</li></ul>| Vytvoří životní událost, když:<br><ul><li>Vytváří se nové zaměstnání a existuje předchozí zaměstnání a mění se typ pracovníka.</li><li>Vytváří se nový údaj zaměstnání a existuje předchozí údaj zaměstnání a mění se typ zaměstnání nebo kategorie zaměstnání.</li><li>Je definována aktualizace záznamu o zaměstnání a jiného typu pracovníka.</li><li>Je zadána aktualizace podrobného záznamu zaměstnání a jiného typu nebo kategorie zaměstnání.</li></ul> |
| **Nové přepsání nároku (nespecifické pro USA)** | **Pokročilé lidské zdroje > Výhody > Plány > Zaměstnanecké výhody > Přepis pravidla nároku** | Použití události zpracování životního cyklu<br>Vytvoření nového přepisu způsobilosti plánu výhod pro pracovníka spustí tuto životní událost.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Změna přepisu pravidla nároku (nespecifické pro USA)** | **Pokročilé lidské zdroje > Výhody > Plány > Zaměstnanecké výhody > Přepis pravidla nároku** | Aktualizace **Platnost od** nebo **Platnost do** na přepsání způsobilosti plánu výhod spustí tuto životní událost. |
| **Vypršení platnosti přepisu pravidla nároku (nespecifické pro USA)** | Správa výhod > Zpracování změn životních událostí  | Tyto životní události jsou vytvořeny z **Zpracování změn životních událostí**. Proces analyzuje zvolené období a právní subjekt a hledá přidružená přepsání nároku na plán výhod. Vytvoří životní události, pokud vypršela platnost přepsání. |
| **Nový plán zaměstnaneckých výhod (nespecifický pro USA)** | **Pokročilé lidské zdroje > Výhody > Plány > Nový** | Možnosti způsobilosti jsou přidány do aktuálního plánu. Je přidán nový plán s připojenými možnostmi způsobilosti.</br></br>Pracovníci HR by v této instanci měli spustit zpracování nároků na události životního cyklu. |
| **Změna přepisu pravidla nároku (nespecifické pro USA)** | **Správa výhod > Pravidla způsobilosti** | Použití zpracování nároku na životní událost. Protokolováno, když se v záznamech **BenefitEligibilityRule** změnily následující hodnoty: **UseEmplCategory**, **UseEmplStatus** nebo **UseEmplType**. Aktualizuje pouze transakce životní události, které již existují pro změněné pravidlo nebo kritéria způsobilosti. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
