---
title: "Nastavit cizí směnky"
description: "Toto téma popisuje kroky k nastavení směnky."
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


Toto téma popisuje kroky k nastavení směnky.

Směnka je písemná nebo elektronická objednávka od zákazníka, který určuje, že jiné strany, obvykle banka platit stanovenou částku společnosti. Při použití směnky k úhradě faktury prodejní objednávky nebo volné faktury účtujete na stranu Dal odběratelského účtu. Tento úvěr je zajištěn směnkou, dokud odběratel směnku neproplatí bance. Obvykle vyrovná fakturu s směnky v den splatnosti. Po příchodu avíza z banky o zaplacení směnky můžete směnku uzavřít. Směnku můžete kreslit u banky na některou z následujících činností:

-   V den splatnosti. Tento přístup je označován jako poslání pro kolekci.
-   Před datem splatnosti obvykle datum skonta, který je určen v platební podmínky, které jsou nastaveny pro zákazníka. Když zaúčtujete transakci, částka slevy je zaúčtována na účet výdajů. Zbývající částka je dluh vůči vám, dokud banka neobdrží platbu od zákazníka. Tento přístup je označován jako poslání pro slevu.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Nastavení účetních profilů pro cizí směnky
Použít **účetní profily odběratelů** stránku nastavit účetní profily, které lze použít s směnky, protestování cizí směnky, úhrady pro shromažďování a úhrady slevy. V **součtový účet** vyberte součtový účet pro zaúčtování částky směnek. Tento účet je připsán na stranu MD nebo na stranu Dal podle typu transakce směnky:
-   Směnky tento účet debetován při zaúčtování směnky a je na stranu Dal při zaúčtování úhrady slevy nebo úhrady pro kolekci.
-   V případě směnečných protestů se účtuje na vrub tohoto účtu při zaúčtování směnečného protestu.
-   V případě inkas plateb se účtuje na vrub tohoto účtu při zaúčtování inkasa platby.
-   V případě úhrady diskontu se účtuje na vrub tohoto účtu při zaúčtování úhrady diskontu.

V **účet vyrovnání** vyberte pokladní účet pro zaúčtování částky směnek. Na vrub tohoto účtu se účtuje při úhradě směnky. V **zálohy DPH** vyberte součtový účet pro zaúčtování částky prodejní daně při použití směnky pro zálohy. V **závazky pro účet slevy** vyberte účet, který chcete účtovat částku slevy pro úhrady pro slevu na. Při zaúčtování úhrady diskontu se účtuje ve prospěch tohoto účtu.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Nastavit účty pohledávek parametry pro cizí směnky
Na **parametry pohledávek** stránky výchozí účetní profily pro cizí směnky jsou vloženy na **hlavní kniha a DPH** kartu. Číselné řady jsou definovány **číselné řady** kartu.
Nastavení názvů deníků pro cizí směnky
------------------------------------------

Na **názvy deníků** stránky, vytvořit alespoň pět názvů deníků pro cizí směnky. Zde jsou typy deníků:
-   **Zákazník vystavení směnky** – vytvořte název deníku pro deník vystavení směnky.
-   **Zákazník Směnečný protest** – vytvořte název deníku pro Deník směnečného protestu.
-   **Zákazník vystavení návratné směnky** – vytvořte název deníku pro deník vystavených návratných cizích směnek.
-   **Bankovní převod odběratele** – vytvořte název deníku pro deník úhrad.
-   **Zákazník vyrovnání směnek** – vytvořte název deníku pro deník vyrovnání cizí směnka.

Na stránce doklad deníku pro každý deník směnky na zadejte informace o směnce **směnky** kartu. Po zaúčtování řádků deníku směnky je lze zobrazit na **dotaz deníku směnek** stránky a **Statistika směnek** stránky.
Nastavení metod platby pro cizí směnky
-----------------------------------------------

Na **metody platby** stránku, nastavit alespoň jednu metodu platby pro cizí směnky. Pokud obchodujete s více než jedné banky, nastavte způsob platby, který odpovídá formát úhrady, která vyžaduje každý bankovní směnky.
Nastavení platebních poplatků pro cizí směnky
-----------------------------------------

Platební poplatek je poplatek spojený s procesem inkasování plateb od odběratelů. Více nastavení platebního poplatku, které řádky mohou být přiřazeny každé platební poplatek. Řádky nastavení lze řídit způsob výpočtu výchozí částky platebních poplatků. Můžete například vytvořit řádky nastavení pro metody platby, určení plateb, měny a časová období. Můžete také vytvořit řádky nastavení pro procento nebo částka, která je založena na denních intervalech. Například můžete nastavit procento úroku, založený na délku, kdy je splatné platby. Pokud bankovní poplatky, jako jsou například různé poplatky za různé typy úhrad, **kolekce** nebo **slevy**, nastavit řádek poplatku samostatnou platbu pro každý typ úhrady.
Nastavení převodních poplatků pro soubory bankovních převodů
------------------------------------------------

Na **bankovní účty** stránky, můžete nastavit úhrady poplatků, které banka účtuje za každého souboru úhrady, která je generována. Převodní poplatky jsou zaúčtovány, když je úhrada potvrzena a jsou známy částky poplatků. Převodní poplatky se liší od platebních poplatků, které jsou získané od zákazníků a spojeny s řádky deníku.
Nastavení rozvržení dokumentů pro cizí směnky
---------------------------------------------

Na **bankovní účty** klepněte na tlačítko **nastavit**a určit rozložení dokumentu, který je požadován pro každý bankovní účet, že bude generovat tištěné směnky doklady pro.
Nastavení odběratelů pro cizí směnky
--------------------------------------

Na **zákazníci** stránky, pro každého zákazníka, který souhlasil s úhradou pomocí směnky, můžete nastavit výchozí metodu platby pro cizí směnky na **výchozí nastavení plateb** kartu.






