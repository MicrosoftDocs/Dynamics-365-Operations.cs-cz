---
title: Vytvoření majetku na základě nákupních objednávek
description: Toto téma vysvětluje, jak lze vytvořit seznam položek dlouhodobého majetku, který lze použít jako základ pro práce údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5068712a7ea1e0d940d4a05a411fb3e1b6f6d9bb9be924d5375b16676561ea1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754100"
---
# <a name="create-assets-based-on-purchase-orders"></a>Vytvoření majetku na základě nákupních objednávek

[!include [banner](../../includes/banner.md)]

 

Toto téma vysvětluje, jak lze vytvořit seznam položek dlouhodobého majetku, který lze použít jako základ pro práce údržby v modulu Správa majetku. Na základě položek majetku můžete zobrazit přehled řádků nákupních objednávek, které byly na těchto položkách vytvořeny. Účelem této funkce je snadné vytvoření majetku ve správě majetku na základě nákupní objednávky.

Nejdříve nastavíte zboží, které bude použito pro vytváření majetku z nákupní objednávky v **položkách majetku**. Po vytvoření řádku nákupní objednávky vytvoříte majetek v části **Čekající majetek**. Je možné rozhodnout, v jaké fázi nákupní objednávky má být majetek vytvořen.


## <a name="select-asset-items"></a>Výběr položek majetku

1. Klikněte na **Správa majetku** > **Nastavení** > **Majetek** > **Zboží**.
2. Klikněte na možnost **Nové**, abyste vytvořili novou položku majetku.
3. V poli **Číslo položky** vyberte položku. Když toto pole opustíte, název položky bude automaticky vložen do pole **Název produktu**.
4. Na pevné záložce **Obecné** vyberte typ majetku pro položku.
5. Vyberte výrobce majetku a model pro položku.
6. Uložte položku.


## <a name="create-assets-from-pending-assets"></a>Vytvoření majetku z čekajícího majetku

1. Klikněte na **Správa majetku** > **Společné** > **Majetek** > **Čekající majetek**.
2. Zobrazí se aktualizovaný přehled nákupních objednávek na základě položek vybraných v okně **Položky majetku**.
3. Můžete filtrovat stav nákupních objednávek a vybrat, ve kterém stavu životního cyklu má být majetek vytvořen. Můžete například chtít vytvořit majetek pouze v případě, že příjemka produktu byla zaúčtována na nákupní objednávce.
4. Vyberte odkaz **Referenční číslo** odkaz na řádku nákupní objednávky a zobrazte detailní informace o zboží.
5. Pokud chcete upravit, které dimenze se zobrazí na pevné záložce **dimenze zásob**, klikněte na tlačítko **Zobrazit dimenze** a vyberte požadované možnosti.
6. Pokud chcete vytvořit majetek na základě řádku nákupní objednávky, zaškrtněte políčko ve sloupci **Značka** pro tento řádek na stránce se seznamem a klikněte na možnost **Vytvořit majetek.** Zobrazí se zpráva s informacemi o ID majetku.
7. Vyberte majetek v seznamu **Všechen majetek** a kliknutím na tlačítko **Upravit** přidejte k majetku Další informace.
8. Pokud chcete odstranit řádek, protože nechcete vytvořit majetek, zaškrtněte v části **Čekající majetek** políčko ve sloupci **Značka** pro tento řádek a klikněte na **Zahodit čekající majetek**. Zobrazí se zpráva s informacemi o ID majetku. Neodstraňujete nákupní objednávku nebo prodejní objednávku, pouze záznam, ze kterého jste mohli vytvořit majetek v modulu **Správa majetku**.

>[!NOTE]
>Všechny dimenze produktu (velikost, barva, konfigurace atd.) jsou automaticky převedeny do atributů majetku. Sledovací dimenze (sériové číslo) jsou při vytvoření majetku uloženy přímo v majetku.


## <a name="find-pending-assets"></a>Vyhledání čekajícího majetku

Můžete spustit **Inventuru čekajícího majetku** ke kontrole čekajícího majetku. Tuto funkci lze například použít k přijetí oznámení pokaždé, když je čekající majetek připraven k vytvoření jako majetek.

1. Klikněte na **Správa majetku** > **Periodická** > **Majetek** > **Inventura čekajícího majetku**.
2. Kliknutím na tlačítko **OK** spusťte úlohu a aktualizujte seznam v okně **Čekající majetek**.
3. Tuto úlohu můžete nastavit tak, aby byla spouštěna jako dávková úloha, například jednou denně.

**Upozornění:** Pokud dojde ke změně dat na nákupní objednávce *poté*, co jste vytvořili majetek na základě příslušející položky, tyto změny se na majetku neprojeví.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]