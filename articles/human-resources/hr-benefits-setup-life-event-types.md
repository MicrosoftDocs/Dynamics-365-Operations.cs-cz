---
title: Konfigurace typů životních událostí
description: Microsoft Dynamics 365 Human Resources používá typy životní události k definování událostí, které jsou platné k aktualizaci přihlášení zaměstnaneckých výhod.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5286bcd940f4068531bae624876c8a35e64db4c3
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741479"
---
# <a name="configure-life-event-types"></a>Konfigurace typů životních událostí

Microsoft Dynamics 365 Human Resources používá typy životní události k definování událostí, které jsou platné k aktualizaci přihlášení zaměstnaneckých výhod. Například svatba nebo narození dítěte. Každý ID typu životní události lze přidružit pouze k jednomu typu životní události. Vytvoříte-li například ID životní události nazvané Změna adresy, která je přidružená k typu životní události, nelze vytvořit další ID s označením změny adresy zaměstnance a spojit je s typem události změny adresy zaměstnance. 

Po vytvoření typů životních událostí je nutné je přidružit k typům plánu. Další informace viz [Vytvoření typů plánů](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Po vytvoření typů životní události je nutné je přidružit k typům plánu. Další informace viz [Vytvoření typů plánů](hr-benefits-setup-life-event-types.md).

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

Můžete zobrazit seznam plánů, které jsou připojeny k vybranému typu životní události. Události životního cyklu jsou připojeny k typu plánu a typy plánů jsou přidruženy k plánu. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **typy životní události**.

2. Vyberte **Akce**.

3. Vyberte **připojené plány**.

## <a name="life-events"></a>Životní události

Při vytváření typu životní události můžete vybrat některou z následujících životních událostí:

| Životní událost | Umístění | Aktivační událost |
| --- | --- | --- |
| **Změna rodinného stavu** | Pracovník> Profil > osobní údaje > Rodinný stav| Změna v rodinném stavu |
| **Změna stavu zaměstnání** | <ul><li>Pracovník > Zaměstnání</li><li>Stránka Historie zaměstnání</li></ul> | Změna stavu zaměstnání |
| **Změna adresy zaměstnance** | <ul><li>Pracovník > Profil > Adresy </li><li>Pracovník > Osobní údaje > Osobní kontaktní > Adresa</li></ul> Přidaná, upravená nebo odstraněná adresa |
| **Změna rodinného příslušníka** | <ul><li>Pracovník > Profil > Osobní údaje > Osobní kontakty > Přidat nebo odstranit závislou osobu</li><li>Samoobsluha pro zaměstnance</li></ul> | Závislá osoba byla přidána nebo odstraněna. Vztah osobního kontaktu musí být dítě, manžel/ka, druh/družka nebo bývalý manžel/manželka. Aktualizace data **Platné od** aktivuje životní událost. Pokud toto datum neaktualizujete, nebude spuštěna žádná životní událost. |
| **Narození nebo adopce (závislá osoba)** | <ul><li>Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě</li><li>Samoobsluha pro zaměstnance</li></ul> | Zadány hodnoty do pole **Datum přijetí**. Je požadováno datum narození dítěte. |
| **Ztráta pokrytí (manžel/ka nebo druh/družka)** | Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě> ztráta pokrytí | **Ztráta pokrytí** vybraná pro osobní kontakt spolu s **datem platnosti** |
| Změna zaměstnání druha/družky | Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě >Zaměstnaná. | <ul><li>Záznam podrobností o závislé osobě vytvořen a pole **Zaměstnaný osobní kontakt** = Ano</li><li>Pole **Zaměstnaný osobní kontakt** změněno (Ano nebo Ne)</li></ul> |
| **Pracovní volno (manžel/ka nebo druh/družka)** | Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě> Pracovní volno | <ul><li>Záznam podobností o závislé úrovni vytvořen a pole**EhrLOAEffectiveDate** vyplněno</li><li>**personPrivateDetails.EhrIsLOA** změněno (ano nebo ne)</li><li>**personPrivateDetails. EhrLOAEffectiveDate** je změněno.</li></ul> |
| **Změna pokrytí (pozice)** | <ul><li>Pracovník -> Přiřazení pozice > Přiřazení pozic pracovníka</li><li>Pozice > Pozice</li></ul> | <ul><li>Změna na pozici v záznamech přiřazení pozice pracovníka</li><li>Změna přiřazení pracovníka na pozici</li></ul> |
| **Zdravotní péče (zaměstnanec / závislá osoba)** | Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě> Datum účinnosti zdravotní péče | Není automaticky spuštěno, pokud osobní kontakt zadá datum platnosti. |
| **Soudně nařízená podpora** | Pracovník > Profil > osobní údaje > Osobní kontakty > Závislá osoba > Podpora nařízená soudem (QMSCO/QDRO a data platnosti | Neaktivuje automatické aktualizace. Neovlivňuje způsobilost; zaznamenává životní událost. |
| **Zemřel/a** | Pracovník> Profil > osobní údaje > Datum úmrtí | Je zadáno datum úmrtí |
| **Důkaz pojištění** | <ul><li>Pracovník > Pracovník > Verze > Historie zaměstnání > Kalendář > Správce dat > Podrobnosti o zaměstnanecké výhodě</li><li> Pracovník > Zaměstnání > Podrobnosti zaměstnaneckých výhod> Datum ověření</li></ul> | <ul><li>Pracovník zadá datum ověření.</li><li>Pracovník nastaví pole EvidenceOfInsurability na hodnotu **Ano**.</li></ul> |
| **Příjemce** | Pracovník > Profil > Osobní údaje > Osobní kontakty | Je přidán osobní kontakt a jsou zadány hodnoty do polí **Příjemce** a **Datum účinnosti**. Osobní kontakt musí být typu **Dítě**, **Manžel/ka**, **DomesticPartner**, **Sourozenec**, **FamilyContact**, **OtherContact**, **Parent**, **BeneficiaryEstate**, **BeneficiaryOrg** nebo **BeneficiaryTrust**. |
| **Lékařská péče zaměstnance** | Pracovník > Pracovník > Verze > Historie zaměstnání > Kalendář > Správce dat > Podrobnosti o zaměstnanecké výhodě | <ul><li>**EhrMedicareEligibilityDate** je změněna.</li><li>**MedicareEligibile** je nastavena na **Ano**</li></ul> |
| **Narozeniny** | Pracovník > Profil > Osobní údaje > Osobní kontakty > Podrobnosti o závislé osobě >Datum narození | Bylo přidáno nebo aktualizováno datum narození (ne po zpracování změny životní události). Příklad: Pokud jsou **možnosti nároku na osobní kontakt** dítěte nastaveny na věk: 26 v nastavení > Výhody > Možnosti nároku osobního kontaktu a v případě, že zaměstnanci HR zpracovávají změny události životního cyklu, zobrazí se zpráva s upozorněním, že závislost není nadále oprávněná pro pokrytí. |
| **Změna nároku pracovníka (netýká se USA)** | <ul><li>Pracovník > Zaměstnání</li><li>Pracovník > pracovník > verze > Historie zaměstnání</li></ul> | <ul><li>Může se změnit typ zaměstnance, kategorie zaměstnání nebo pět polí nároku podle uživatele.</li><li>Změny **HcmEmploymentDetail.EhrEmploymentType** (zpracované jen pro *změněné* záznamy podrobností o zaměstnání, nezpracované pro *nové* záznamy o zaměstnání, jako opětovné přijetí do pracovního poměru a výpověď)</li></ul> |
| **Nové přepsání nároku (nespecifické pro USA)** | Pokročilé lidské zdroje > Výhody > Plány > Zaměstnanecké výhody > Přepis pravidla nároku | Použití události zpracování životního cyklu | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Změna přepisu pravidla nároku (nespecifické pro USA)** | Pokročilé lidské zdroje > Výhody > Plány > Zaměstnanecké výhody > Přepis pravidla nároku | Použití zpracování události životního cyklu (zachytí pouze změny polí **ValidFrom** a **ValidTo** v přepisu pravidla způsobilosti) |
| **Vypršení platnosti přepisu pravidla nároku (nespecifické pro USA)** | Pokročilé lidské zdroje > Výhody > Plány > Zaměstnanecké výhody > Přepis pravidla nároku | Použití zpracování životní události. Pokud například upravíte datum vypršení platnosti pravidla způsobilosti plánu na hodnotu 5:00 odp., kdykoliv po 5:00 odp. nebo v následujících dnech, a poté spustíte zpracování změny události životního cyklu, zobrazí se zpráva oznamující, že platnost přepisu pravidla způsobilosti vypršela. |
| **Nový plán zaměstnaneckých výhod (nespecifický pro USA)** | Pokročilé lidské zdroje > Výhody > Plány > Nový | <ul><li>Možnosti způsobilosti jsou přidány do aktuálního plánu.</li><li>Je přidán nový plán s připojenými možnostmi způsobilosti.</li></ul></br></br>Pracovníci HR by v této instanci měli spustit zpracování nároků na události životního cyklu. |
| **Změna přepisu pravidla nároku (nespecifické pro USA)** | Pokročilé lidské zdroje > Výhody > Pravidla/možnosti > Pravidla zaměstnaneckých výhod | Použití zpracování nároku na životní událost. Protokolováno, když se v záznamech **EhrBenefitEligibilityRule** změnily následující hodnoty: **UseEmplCategory**, **UseEmplStatus** nebo **UseEmplType**. Aktualizuje pouze transakce životní události, které již existují pro změněné pravidlo nebo kritéria způsobilosti. |
