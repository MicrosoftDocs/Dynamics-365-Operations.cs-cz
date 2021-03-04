---
title: Kusovníky majetku
description: Toto téma popisuje kusovníky majetku ve správě majetku.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f42646ae865cd530203c997fd10c8ccd59e7fa2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423950"
---
# <a name="asset-boms"></a>Kusovníky majetku

[!include [banner](../../includes/banner.md)]

 

Toto téma popisuje kusovníky majetku ve správě majetku. Stránka **Kusovník majetku** zobrazuje seznam všech položek (náhradních dílů a jiných položek), které jsou použity v majetku po celou dobu jeho životnosti. Při vytváření nového majetku byste měli zvážit nastavení kusovníku majetku jako součásti postupu nastavení. Tímto způsobem můžete sledovat historii položek majetku od data vytvoření.

Po dokončení úlohy údržby a registraci spotřeby položky na pracovním příkazu můžete sledovat spotřebu náhradních dílů a dalších položek, které jsou u majetku použity. Tato funkce umožňuje uchovávat kompletní záznam spotřeby položky pro všechny majetky. Pomocí tohoto záznamu můžete například sledovat, zda je určitý náhradní díl často vyměňován, nebo sledovat náhradní díly nebo jiné položky, které jsou u majetku aktuálně použity.

> [!NOTE]
> Na pracovním příkazu může spotřeba položky zahrnovat jak náhradní díly, tak i další položky, jako jsou maziva, šrouby a těsnění.

Kusovník majetku může být automaticky aktualizován na základě nastavení správy majetku. Pokud byl stav životního cyklu pracovního příkazu vytvořen pro zpracování dokončených pracovních příkazů a pokud je možnost **Aktualizovat kusovník majetku** stav životního cyklu pracovního příkazu nastaven na **Ano** na stránce **Stav životního cyklu pracovního příkazu**, budou všechny položky použité na pracovním příkazu automaticky aktualizovány na stránce **Kusovník majetku**, když je pracovní příkaz aktualizován do tohoto stavu životního cyklu. 


Můžete také ručně aktualizovat kusovník majetku vytvořením nových řádků položek na stránce **Kusovník majetku**.

Na stránce **Kusovník majetku** můžete sledovat historii náhradních dílů pro majetek po registraci spotřeby položky na pracovním příkazu. Chcete-li použít tuto funkci, musíte vybrat skupiny položek, které by měly být použity pro registraci náhradních dílů na stránce **Skupiny položek náhradních dílů**.

Chcete-li použít funkci kusovníku majetku, musíte nejprve nastavit požadované skupiny položek náhradních dílů. Pokud pak chcete, aby byl kusovník majetku po dokončení pracovního příkazu automaticky aktualizován, můžete nastavit stav životního cyklu pracovního příkazu pro zpracování této aktualizace. 


## <a name="set-up-spare-parts-item-groups"></a>Nastavení skupin položek náhradních dílů

Nastavení historie náhradních dílů je založeno na skupinách položek vytvořených v modulu **Řízení zásob a skladu**. Ve správě majetku nastavíte skupiny položek tak, aby bylo možné sledovat historii náhradních dílů pro položky ve vybraných skupinách položek.

1. Vyberte **Sráva majetku** \> **Nastavení** \> **Majetek** \> **Skupiny položek náhradních dílů**.
2. Vyberte **Nová**, chcete-li nastavit skupinu položek.
3. V poli **Skupina položky** vyberte skupinu. Název skupiny se automaticky vyplní do pole **Název**.

## <a name="view-and-update-asset-boms"></a>Zobrazení a aktualizace kusovníků majetku

Po zaúčtování spotřeby položky na pracovním příkazu můžete zobrazit registrovanou spotřebu položky na stránce **Kusovník majetku**.

1. Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Aktivní majetek**. Vyberte majetek v seznamu a pak vyberte **Kusovník majetku**.

    > [!NOTE]
    > Chcete-li zobrazit všechny registrace spotřeby položek u veškerého majetku, vyberte **Správa majetku** \> **Dotazy** \> **Majetek** \> **Kusovník majetku**.

2. Vyberte **Aktualizovat kusovník majetku**. Do aktualizace můžete přidat majetek, typy majetku a zdroje podle potřeby volbou možnosti **Vybrat**. Vyberte **OK** a spusťte aktualizaci. Funkci aktualizace můžete také nastavit jako dávkovou úlohu.
3. Pokud chcete zobrazit více informací vztahujících se k položkám, můžete přidat dimenze zásob. Vyberte **Zásoby** \> **Zobrazení dimenzí** a pak zaškrtněte políčka u dimenzí, které chcete zobrazit. Chcete-li zachovat toto nastavení pro všechen majetek na stránce **Kusovník majetku**, nastavte možnost **Uložit nastavení** na **Ano**.
4. Chcete-li získat přehled o tom, kde se ve správě majetku používá položka na vybraném řádku, ve vztahu k majetku, výchozím typům práce, náhradním dílům a pracovním příkazům, vyberte **Položka, kde se používá**. 
5. Pokud chcete zobrazit pouze řádky aktivních položek, vyberte **Zobrazit** \> **Aktuální**. Chcete-li zobrazit všechny řádky položek, včetně řádků, kde je datum vypršení platnosti dřívější než aktuální datum, vyberte **Zobrazit** \> **Vše**.

> [!NOTE]
> Po dokončení pracovního příkazu, pokud vypršela platnost některých položek nebo náhradních dílů, které souvisejí se souvisejícím majetkem nebo byly nahrazeny jinými položkami nebo náhradními díly, doporučujeme odpovídajícím způsobem aktualizovat kusovník majetku.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Vytvoření nového řádku položky v kusovníku majetku

Pro majetek můžete ručně vytvořit řádky položky.

1. Na stránce **Kusovník majetku** zvolte **Nový**.
2. V poli **Majetek** vyberte majetek, pro který chcete přidat řádek položky.
3. Do pole **Číslo řádku** zadejte pořadové číslo řádku.
4. V poli **Platnost** zadejte počáteční datum pro položku.
5. Pokud platnost položky vyprší, zadejte do pole **Vypršení platnosti** koncové datum.
6. V poli **Číslo položky** vyberte položku. Název se automaticky vyplní do pole **Název produktu**.
7. Poté v poli **Množství** zadejte množství, které se používá. Pole **Jednotka** je aktualizováno automaticky.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]