---
title: "Konfigurace modulu Závazky"
description: "Tento článek popisuje stránky, které slouží k nastavení základních a volitelných funkcí pro modul Závazky v aplikaci Microsoft Dynamics AX. Dále popisuje postup nastavení, který musíte dokončit dříve, než začnete nastavovat modul Závazky."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: b06623a0eb754654f41c50b92af67dc94a069663
ms.lasthandoff: 03/31/2017


---

# <a name="configure-accounts-payable"></a>Konfigurace modulu Závazky

[!include[banner](../includes/banner.md)]


Tento článek popisuje stránky, které slouží k nastavení základních a volitelných funkcí pro modul Závazky v aplikaci Microsoft Dynamics AX. Dále popisuje postup nastavení, který musíte dokončit dříve, než začnete nastavovat modul Závazky.

<a name="prerequisites-for-accounts-payable-setup"></a>Předpoklady k nastavení modulu Závazky
----------------------------------------

Před nastavením modulu Závazky je nutné provést tyto úkoly:

-   V hlavní knize:
    -   Máte-li v úmyslu používat deníky plateb, nastavte je.
    -   Pokud máte v úmyslu spouštět vyrovnání kurzových rozdílů, na stránce Měny nastavte kódy měn, na stránce Typy směnného kurzu nastavte typy směnných kurzů a na stránce Směnné kurzy měn nastavte směnné kurzy měn.
-   V modulu Pokladna a banka nastavte bankovní účty, které se mají používat pro metody platby.

## <a name="setup-pages-for-accounts-payable"></a>Nastavení stránky pro závazky

Následující stránky slouží k nastavení základních funkcí modulu Závazky pro jednotlivé právní osoby. Stránky jsou uvedeny v doporučeném pořadí nastavení. Pro zjednodušení procesu nastavení si můžete z prvních vytvořených záznamů vytvořit šablony. Šablona obvykle obsahuje hodnoty pro velký počet polí, které odpovídají funkcím, jež chce organizace implementovat pro určitý typ dodavatelů.
1.  Stránka Platební podmínky slouží k určení platebních podmínek, které chcete přiřadit prodejním objednávkám, nákupním objednávkám, odběratelům a dodavatelům a které určují data splatnosti faktur.
2.  Stránka Způsob platby – dodavatelé slouží k vytvoření a správě informací o tom, jak organizace platí svým dodavatelům.
3.  Stránka Skupiny dodavatelů slouží k vytváření a údržbě skupin dodavatelů se společnými důležitými parametry pro účtování, vyrovnávání, platby, vykazování a prognózy.
4.  Stránka Účetní profily dodavatele slouží k určení toho, jak jsou transakce dodavatelů zaúčtovány do hlavní knihy.
5.  Stránka Parametry závazků slouží k nastavení výchozích parametrů používaných v případě, že pro modul Závazky není zadáno specifičtější nastavení, parametry různých typů funkcí a různé číselné řady.
6.  Stránka Nastavení formuláře slouží k určení formátu různých dokumentů souvisejících s dodavateli, které organizace používá ke sledování příjemek od dodavatelů a k zadávání důvodů pro toky plateb k dodavatelům.
7.  Stránka Dodavatelé slouží k vytváření a údržbě účtů dodavatelů a také finančních úřadů, jimž vaše organizace odevzdává výkazy DPH.

## <a name="optional-setup-pages-for-accounts-payable"></a>Volitelné nastavení stránky pro závazky
Kromě základních funkcí má modul Závazky další funkce, které lze nastavit.

Další stránky pro nastavení jsou uspořádány podle funkcí.

**Policies**
-   Stránka Zásada faktur dodavatele slouží k nastavení zásad pro faktury dodavatele.

**Invoice matching**

-   Stránka Tolerance součtu faktur slouží k nastavení tolerancí pro celkové hodnoty faktur.
-   Stránka Zásady párování slouží k nastavení zásad dvoucestného a třícestného párování.
-   Stránka Tolerance ceny slouží k nastavení tolerance pro jednotkové ceny.
-   Stránka Skupiny tolerance ceny položky slouží k nastavení skupin tolerancí pro ceny položky.
-   Stránka Skupiny tolerance ceny dodavatele slouží k nastavení skupin tolerancí pro ceny dodavatele.
-   Stránka Tolerance nákladů slouží k nastavení tolerance pro náklady.

**Workflow**

-   Stránka Workflowy závazků slouží k úpravě konfigurace workflowu pro schvalování deníků a nákupních žádanek.

**Reasons**

-   Stránka Dodavatel – důvody slouží k nastavení kódů důvodů.

**Charges**

-   Stránka Kód nákladů slouží k nastavení kódů pro náklady, které se používají v nákupních objednávkách.
-   Na stránce skupina nákladů dodavatele vytvoření a udržování skupin nákladů pro dodavatele.
-   Stránka Skupiny nákladů zboží slouží k vytváření a správě skupin nákladů pro položky..
-   Stránka Automatické doprovodné náklady slouží k určení nákladů, které jsou automaticky přiřazeny k objednávkám.

**Supplementary items**

-   Stránka Skupiny doplňkových položek – dodavatel slouží k vytváření a správě skupin doplňkových položek pro dodavatele.
-   Stránka Skupiny doplňkových položek – zásoby slouží k vytváření a správě skupin doplňkových položek pro položky.

**Distribution**

-   Stránka Dodací podmínky slouží k vytvoření a správě podmínek pro převod položky od prodávajícího ke kupujícímu.
-   Stránka Způsoby dodání slouží k vytváření a správě způsobů přepravy, které se používají při doručování objednávky od prodávajícího ke kupujícímu.
-   Stránka Kódy místa určení slouží k vytváření a správě identifikátorů a popisů míst určení.

**Forms**

-   Stránka Poznámky na formulářích slouží k vytváření a správě standardního textu, který se zobrazuje na různých stránkách.
-   Stránka Parametry třídění formuláře slouží k nastavení pořadí řazení požadavků, příjemek, dodacích listů a faktur.
-   Stránka Nastavení správy tisku slouží k nastavení informací správy tisku pro originály a kopie stránek.

**Payments**

-   Stránka Platební slevy slouží k nastavení a správě podmínek pro získání platebních slev. Kódy platebních slev jsou propojeny s dodavateli a použity v nákupních objednávkách.
-   Stránka Platební kalendáře slouží k nastavení platebních kalendářů, které se používají ke správě splátkových plateb dodavatelům.
-   Stránka Dny platby slouží k určení dnů platby, které se používají k výpočtu dat splatnosti, a k určení dnů platby pro určité dny v týdnu nebo měsíci.
-   Stránka Platební poplatek slouží k vytváření a správě platebních poplatků přiřazených k dodavatelům.
-   Stránka Platební instrukce slouží k vytváření a správě platebních instrukcí.

**Statistics**

-   Stránka Definice období pro sledování splatnosti slouží k nastavení uživatelem definovaných intervalů, které se používají pro analýzu rozložení splatnosti dodavatelských účtů.
-   Stránka Odvětví obchodu slouží k vytváření kódů odvětví obchodu (LOB), které jsou přiřazeny k dodavatelům.

**Daně 1099**

-   Na **polí 1099** stránky, ověření a aktualizaci minimální částky, které musí být uvedeny na interní výnosy služby (finanční úřad), podle nejnovějších požadavků finančního úřadu.

## <a name="optional-setup-for-other-modules"></a>**Volitelné nastavení pro ostatní moduly**
**Organization administration**

-   Stránka Číselné řady slouží k nastavení skupin číselných řad pro čísla faktur.
-   Na následujících stránkách nastavíte informace o adrese:
    -   Nastavení adresy
    -   Kódy NAF
    -   Importovat PSČ

**General ledger**

-   Stránka Finanční dimenze slouží k nastavení finančních dimenzí.
-   Na následujících stránkách nastavíte informace o daních:
    -   Kódy DPH
    -   Skupiny DPH
    -   Skupiny DPH položky
    -   Účetní skupina
    -   Kódy osvobození od DPH
    -   Příslušnosti k dani
    -   Finanční úřady
    -   Období vyrovnání DPH

**Cash and bank management**

-   Stránka Kódy účelu platby slouží k nastavení kódu účelu centrální banky.





