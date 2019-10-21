---
title: Vratka DPH ve správě výdajů
description: Toto téma vysvětluje postup refundace u transakcí s nárokem na vrácení daně z přidané hodnoty.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70a53282bf1d140cb24108fe98e48aa82f783be5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176784"
---
# <a name="vat-recovery-in-expense-management"></a>Vratka DPH ve správě výdajů

[!include [banner](../includes/banner.md)]

Chcete-li získat refundaci za transakce s nárokem na vrácení daně z přidané hodnoty, musí společnost nebo organizace identifikovat, shromažďovat, ověřovat a odesílat přesné informace. Tento proces zahrnuje více úloh a podle velikosti společnosti může zahrnovat několik zaměstnanců nebo rolí.

Chcete-li získat zpět DPH pomocí správy nákladů, musíte splnit následující předpoklady:

- Pro země/oblasti, které jsou přiděleny do kategorií výdajů, je třeba vytvořit daňové kódy.
- Pro každý daňový kód musí být vytvořena skupina DPH.
- Pro každou skupinu DPH musí být vytvořena položka kódu DPH.

Po dokončení předpokladů zaměstnanci postupují podle těchto kroků, aby požádali o vrácení DPH.

1. V sestavě výdajů zadejte daňové informace o transakcích platebních karet pro identifikaci vrácení nárokovatelné DPH.
2. Ujistěte se, že jsou všechny daňové informace dokončeny, a poté zaúčtujte sestavu výdajů.
3. Zpracujte výdaje způsobilé pro mezinárodní vratku DPH.
4. Odešlete údaje o navrácení DPH dodavateli třetí strany za účelem podání mezinárodních vratek.
5. Zpracujte výdaje pro domácí vratky DPH.

Následující části obsahují příklady, které zobrazují způsob, jakým zaměstnanci společnosti Contoso dokončují jednotlivé kroky.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>V sestavě výdajů zadejte daňové informace o transakcích platebních karet pro identifikaci vrácení nárokovatelné DPH.

Nancy, prodejní zástupce společnosti Contoso se sídlem v USA, se nedávno vrátila z obchdodní cesty do Spojeného království. Během její cesty jí vznikly některé výdaje za stravování placené osobní kreditní kartou. Nancy musí nyní vytvořit sestavu výdajů pro odsouhlasení svých výdajů.

Nancy zadá informace do své sestavy výdajů a vybere **Spojené království** v poli **Země/oblast** na stránce **Upravit sestavu výdajů**. Seznam skupin DPH je poté filtrován tak, aby zobrazoval pouze skupiny, které platí pro Velkou Británii. Nancy vybere skupinu DPH **Spojené království 001** a poté vybere skupinu DPH položky **Jídla**. Poté přidá novou transakci za své ubytování. Vzhledem k tomu, že ve Spojeném království existuje pouze jedna skupina DPH a jedna skupina DPH položky, tyto informace budou automaticky vyplněny do její sestavy výdajů.

Podle zásad společnosti Contoso musí mít všechny výdaje odpovídající účtenku. Proto když Nancy uloží svou sestavu výdajů, obdrží zprávu oznamující, že musí připojit účtenku pro každou transakci, kteráou uvedla ve svém vyúčtování výdajů. Anna ověří, že připojila ke svému vyúčtování výdajů naskenovaný obrázek všech účtenek transakcí, a odešle svou sestavu ke schválení. Poté odešle papírové účtenky účetnímu týmu. Tento tým odešle data pro vratku DPH dodavateli třetí strany, který podá pro společnost Contoso mezinárodní vratku DPH.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Ujistěte se, že jsou všechny daňové informace dokončeny, a poté zaúčtujte sestavu výdajů.

Anna, koordinátorka závazků společnosti Contoso, musí zadat všechny daňové informace, které ve vyúčtování výdajů chybí, než může být sestava zaúčtována. Otevře stránku **Podrobnosti o sestavě výdajů** a vidí schválené vyúčtování výdajů od Nancy. Anna potom otevře sestavu výdajů pro zobrazení podrobností o transakcích. Zjistí, že Nancy nezadala skupinu DPH položky pro jednu z transakcí. Vzhledem k tomu, že tento údaj není uveden, Anna nemůže zaúčtovat sestavu výdajů. Proto se Anna podívá na stránku **Konfigurace daní** v modulu Správa výdajů a vyhledá příslušnou skupinu DPH položky pro danou zemi/oblast a typ transakce. Nyný může Anna zaúčtovat sestavu výdajů do hlavní knihy

Když Anna zaúčtuje sestavu výdajů, vytvoří se pracovní položka vratky DPH. Tato pracovní položka je přiřazena členovi účetního týmu. Anna obdrží zprávu, která potvrzuje, že zaúčtování proběhlo úspěšně. Tato zpráva obsahuje také seznam s počtem transakcí DPH, které byly určeny pro vratku.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Zpracování výdajů způsobilých pro mezinárodní vratku DPH

Arnold, člen účetního týmu společnosti Contoso, je zodpovědný za potvrzení, že všechny požadované informace pro vratku DPH jsou zahrnuty ve vyúčtování výdajů. Otevře stránku **Výdajová vratka daně** a vybere sestavu výdajů, kterou Nancy odeslala. Arnold ověří, že jsou připojeny všechny požadované účtenky a že byla správně zadána skupina DPH a kódy DPH položky.

Když Arnold obdrží papírové účtenky od Nancy, ověří je oproti digitálním účtenkám a změní stav sestavy výdajů na **Připraveno pro vratku**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Odeslání údajů o navrácení DPH dodavateli třetí strany za účelem podání mezinárodních vratek

Když je Arnold připraven odeslat data sestavy výdajů dodavateli třetí strany, který podá vratku DPH vrátí, otevře stránku **Výdajová vratka daně**. Vyfiltruje stránkuy tak, aby se zobrazily pouze sestavy výdajů, které jsou označené jako **Připraveno pro vratku**. Poté vybere Arnold položky **Soubor** &gt; **Exportovat do aplikace Excel**. Informace o DPH ze sestavy výdajů jsou exportovány do listu aplikace Microsoft Excel. Arnold odešle tento list dodavateli třetí strany a přidá zprávu, která oznamuje, že papírové účtenky byly odeslány kurýrem.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Zpracování výdajů pro domácí vratky DPH

Arnold musí ověřit, zda jsou transakce vyúčtování výdajů nárokovatelné na vratku DPH a zda jsou digitální účtenky připojeny k sestavám. Aby mohl zahájit zpracování výdajů s nárokem na domácí vratku, otevře Arnold stránku **Výdajová vratka daně** a vybere vyúčtování výdajů, které vyžaduje ověření. Zkontroluje, zda jsou účtenky na jméno společnosti, nikoliv zaměstnance. Pro vrácení DPH musí být účtenky na jméno společnosti. Arnold pak potvrdí, že byla použita správná skupina DPH a kódy DPH položky.

Když Arnold dostane papírové účtenky, změní stav vyúčtování výdajů na **Připraveno pro vratku**. Poté můžete podat vratku u příslušného daňového úřadu. V tomto případě je příslušný finanční úřad v USA Internal Revenue Service (IRS).
