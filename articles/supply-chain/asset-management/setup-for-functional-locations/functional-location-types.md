---
title: Typy funkčního místa
description: Tento článek popisuje, jak vytvořit typy funkčních míst v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8276d77f7655659cab13f3c520d7c171e3cfd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879214"
---
# <a name="functional-location-types"></a>Typy funkčního místa

[!include [banner](../../includes/banner.md)]

 

Tento článek popisuje, jak vytvořit typy funkčních míst v modulu Správa majetku. Typy funkčních míst se používají ke správě požadavků na funkční místa, včetně způsobu instalace majetku na funkčním místo. Můžete nastavit typy majetku, plány údržby, atributy funkčních míst a požadavky atributů majetku, které mají být použity na funkčním místě, které používá konkrétní typ funkčního místa. Pokud vytvoříte funkční místo, je typ místa funkčního místa povinný.

>[!NOTE] 
>Chcete-li pracovat s funkčními místy, je nutné vytvořit výchozí funkční místo, které bude použito pouze pro účely vytvoření nového majetku. Pro toto výchozí funkční místo byste měli vytvořit výchozí typ funkčního místa, který je opravdu jednoduchý a umožňuje instalaci vícero majetků do výchozího funkčního místa. Viz [Vytvoření funkčních míst](../functional-locations/create-functional-locations.md) pro více informací o nastavení funkčních míst.

## <a name="create-a-default-functional-location-type"></a>Vytvoření výchozího typu funkčního místa

Tento postup ukazuje, jak vytvořit výchozí typ funkčního místa, který bude použit pro výchozí funkční místo.

1. Vyberte **Správa majetku** > **Nastavení** > **Funkční místa** > **Typy funkčního místa**.
2. Zvolte **Nový** pro vytvoření typu funkčního místa.
3. Do pole **Typ funkčního místa** vložte ID typu funkčního místa, například Výchozí, a název do pole **Název**.
4. Zvolte model životního cyklu v poli **Model životního cyklu funkčních míst**.
5. Chcete-li povolit instalaci vícero majetku do funkčního místa (výchozí funkční místo) pomocí tohoto typu, zvolte Ano na přepínacím tlačítku **Více majetků**.

Nyní je vytvořen výchozí typ funkčního místa, který se použije pouze na výchozí funkční místo. Neměli byste přidávat žádné další požadavky nebo omezení na tento výchozí typu funkčního místa.


## <a name="create-functional-location-types"></a>Vytvoření typů funkčních míst

1. Vyberte **Správa majetku** > **Nastavení** > **Funkční místa** > **Typy funkčního místa**.
2. Zvolte **Nový** pro vytvoření typu funkčního místa.
3. Do pole **Typ funkčního místa** vložte ID typu funkčního místa a název do pole **Název**.
4. Zvolte model životního cyklu v poli **Model životního cyklu funkčních míst**. Další informace o stavech životního cyklu funkčních míst a modelech životního cyklu naleznete v tématu [Stavy životního cyklu funkčních míst](../setup-for-functional-locations/functional-location-stages.md).
5. Zvolte Ano na přepínacím tlačítku **Více majetků**, pokud má být možné instalovat několik majetků na funkční místo pomocí tohoto typu funkčního místa. Pokud vyberete možnost Ne, můžete pomocí tohoto typu funkčního místa nainstalovat pouze *jeden* majetek na funkční místo.
6. Chcete-li, aby majetek byl nainstalován na funkčním místě tohoto typu pro automatické použití finančních dimenzí vztahujících se k funkčnímu místu, zvolte Ano na přepínacím tlačítku **Aktualizovat dimenzi majetku**. To znamená, že pokud změníte finanční dimenze ve formuláři [Vytvoření funkčních míst](../functional-locations/create-functional-locations.md) a funkční místo používá typ funkčního místa s tímto přepínacím tlačítkem nastaveným na Ano, finanční dimenze se automaticky aktualizují u všech majetků instalovaných v tomto funkčním místě.
7. Pole **Typ majetku** se používá v případě, že chcete automaticky vytvořit *jeden* majetek pro funkční místo se stejným ID a názvem jako vytvářené funkční místo. To může být důležité například v případě, že vytvoříte statické funkční místo, například budovu nebo potrubí. V takovém případě vyberte typ majetku, který chcete použít pro automaticky vytvořený majetek. Mějte na paměti, že pokud v tomto poli provedete výběr, musí být přepínací tlačítko nastaven na **Více majetků**.
8. Na záložce s náhledem **Typy majetku** vyberte typy majetku, které mají souviset s typem funkčního místa. Vyberte **Přidat řádek** a vyberte typy majetku. Pokud sem přidáte typy majetku, mohou být pomocí tohoto typu funkčního místa na funkčním místě nainstalovány pouze majetky používající tyto typy majetku. Pokud nejsou na záložce s náhledem **Typy majetku** zvoleny žádné typy majetku, mohou být nainstalovány všechny typy majetku.
9. Na záložce s náhledem **Plány údržby** vyberte plány údržby, které mají být automaticky nastaveny na nových funkčních místech pomocí tohoto typu funkčního místa. Vyberte **Přidat řádek** a vyberte plány údržby. Přidáte-li sem plány údržby, lze použít pouze tyto plány na funkčním místě s použitím tohoto typu funkčního místa.
10. Na záložce s náhledem **Požadavky na atributy majetku** nastavte atributy majetku, které mají být automaticky nastaveny na nových funkčních místech pomocí tohoto typu funkčního místa. Vyberte **Přidat řádek** a vyberte atribut. Tyto požadavky na atributy fungují jako pokyny. Nejsou ověřeny vůči atributům, které jsou nastaveny u majetku (**Správa majetku** > **Společné** > **Majetek** > **Všechen majetek** > zvolte majetek na stránce se seznamem, karta > **Obecné** > tlačítko **Atributy**). Požadavky na atributy se zobrazí při instalaci majetků na funkční místa.
11. Na záložce s náhledem **Povolené typy** vyberte typy funkčních míst, které by měly být platné pro dílčí typy funkčních míst související s nadřazeným typem funkčního místa, který používá vybraný typ funkčního místa.
12. Na záložce s náhledem **Atributy** vyberte atributy funkčního místa, které mají být automaticky nastaveny na funkčních místech pomocí tohoto typu funkčního místa. Vyberte **Přidat řádek** a vyberte atribut.


>[!NOTE] 
>Na záložce s náhledem **Obecné** můžete získat přehled o počtu typů majetku, plánech údržby, požadavcích na atributy majetku, povolených typech, atributech a funkčních místech nastavených u typu funkčního místa. Pole **Funkční místa** zobrazuje počet funkčních míst, který používá typ funkčního místa. Pomocí tlačítka **Kopírovat** můžete kopírovat nastavení z typu funkčního místa do vybraného typu funkčního místa.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]