---
title: "Nastavit cizí směnky"
description: "Toto téma popisuje kroky k nastavení směnek."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Nastavit cizí směnky

[!include[banner](../includes/banner.md)]


Toto téma popisuje kroky k nastavení směnek.

Směnka představuje písemný nebo elektronický příkaz odběratele určující, že jiná strana, obvykle banka, musí společnosti zaplatit uvedenou částku. Při použití směnky k úhradě faktury prodejní objednávky nebo volné faktury účtujete na stranu Dal odběratelského účtu. Tento úvěr je zajištěn směnkou, dokud odběratel směnku neproplatí bance. Obvykle hradíte fakturu směnkou ke dni splatnosti. Po příchodu avíza z banky o zaplacení směnky můžete směnku uzavřít. Směnka může projít bankou v jednom z následujících časů:

-   V den splatnosti. Tento přístup se nazývá odesláno k inkasu.
-   Před datem splatnosti, obvykle k datu slevy, které je upřesněné v platebních podmínkách nastavených pro odběratele. Když zaúčtujete transakci, částka slevy je zaúčtována na účet výdajů. Zbývající částka je dluh vůči vám, dokud banka neobdrží platbu od zákazníka. Tento přístup se nazývá poukázat k diskontu.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Nastavení účetních profilů pro cizí směnky
Stránka **Účetní profily odběratelů** slouží k nastavení účetních profilů, které můžete použít se směnkami, směnečnými protesty, inkasy plateb a úhradami diskontu. V poli **Součtový účet** vyberte souhrnný účet, na který budou účtovány částky směnek. Podle typu transakce směnky je z toho účtu částka stržena nebo je na něj připsána:
-   V případě směnek se při zaúčtování směnky účtuje na vrub tohoto účtu. Ve prospěch účtu se účtuje při zaúčtování úhrady diskontu nebo inkasa platby.
-   V případě směnečných protestů se účtuje na vrub tohoto účtu při zaúčtování směnečného protestu.
-   V případě inkas plateb se účtuje na vrub tohoto účtu při zaúčtování inkasa platby.
-   V případě úhrady diskontu se účtuje na vrub tohoto účtu při zaúčtování úhrady diskontu.

V poli **Účet vyrovnání** vyberte peněžní účet, na který budou zaúčtovány částky směnek. Na vrub tohoto účtu se účtuje při úhradě směnky. V poli **Zálohy DPH** vyberte souhrnný účet, na který budou zaúčtovány částky DPH na výstupu, pokud se směnky používají pro zálohové platby. V poli **Závazky pro účet slevy** vyberte účet pro zaúčtování částky diskontu pro úhrady diskontu. Při zaúčtování úhrady diskontu se účtuje ve prospěch tohoto účtu.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Nastavení parametrů pohledávek pro cizí směnky
Na stránce **Parametry pohledávek** se výchozí účetní profily pro cizí směnky zadávají na kartě **Hlavní kniha a DPH**. Číselné řady se definují na kartě **Číselné řady**.
Nastavení názvů deníků pro cizí směnky
------------------------------------------

Na stránce **Názvy deníků** vytvořte alespoň pět názvů deníků pro cizí směnky. Typy deníků jsou následující:
-   **Vystavení cizí směnky odběratelem** – vytvořte název deníku pro deník vystavení cizí směnky.
-   **Odběratel – protestovat cizí směnku** – vytvořte název deníku pro deník směnečného protestu.
-   **Odběratel – vystavit cizí návratnou směnku** – vytvořte název deníku pro deník vystavených návratných cizích směnek.
-   **Bankovní převod odběratele** – vytvořte název deníku pro deník úhrad.
-   **Odběratel – vyrovnat cizí směnku** – vytvořte název deníku pro deník vyrovnání cizích směnek.

Na stránce dokladu deníku pro každý deník cizí směnky zadejte informace o cizí směnce na kartě **Cizí směnka**. Po zaúčtování řádků deníku cizí směnky je lze zobrazit na stránce **Dotaz deníku na cizí směnku** a stránce **Statistika směnek**.
Nastavení metod platby pro cizí směnky
-----------------------------------------------

Na stránce **Metody platby** nastavte alespoň jednu metodu platby pro cizí směnky. Jestliže spolupracujete s několika bankami, nastavte metody platby tak, aby odpovídaly formátu úhrady, který každá banka pro cizí směnku požaduje.
Nastavení platebních poplatků pro cizí směnky
-----------------------------------------

Platební poplatek je poplatek spojený s procesem inkasování plateb od odběratelů. Každý platební poplatek může mít přiřazeno několik nastavených řádků poplatků. Můžete použít řádky nastavení pro stanovení výpočtu výchozích částek platebních poplatků. Můžete například vytvořit řádky nastavení pro metody platby, určení plateb, měny a časová období. Můžete také vytvořit řádky nastavení pro procento nebo částku, které jsou založeny na denních intervalech. Například můžete nastavit procento úroku založené na délce období, kdy je platba po splatnosti. Účtuje-li banka různé poplatky u různých typů úhrad, jako jsou **Kolekce** nebo **Sleva**, nastavte samostatný řádek platebního poplatku pro každý typ úhrady.
Nastavení převodních poplatků pro soubory bankovních převodů
------------------------------------------------

Pro každý generovaný soubor úhrad lze nastavit převodní poplatky účtované bankou na stránce **Bankovní účty**. Převodní poplatky jsou zaúčtovány, když je úhrada potvrzena a jsou známy částky poplatků. Převodní poplatky se liší od platebních poplatků, které se inkasují od odběratelů a jsou připojeny k řádkům deníku.
Nastavení rozvržení dokumentů pro cizí směnky
---------------------------------------------

Pro každý bankovní účet, ze kterého budete generovat tištěné směnky, upřesněte požadované rozvržení dokumentu kliknutím na položku **Nastavit** na stránce **Bankovní účty**.
Nastavení odběratelů pro cizí směnky
--------------------------------------

Pro každého odběratele, který souhlasil s úhradou prostřednictvím směnky, můžete nastavit výchozí metodu platby pro cizí směnky na stránce **Odběratelé** na kartě **Výchozí nastavení plateb**.






