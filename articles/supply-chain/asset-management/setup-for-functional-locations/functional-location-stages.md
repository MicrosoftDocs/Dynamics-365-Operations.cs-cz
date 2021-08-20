---
title: Stavy životního cyklu funkčních míst
description: Toto téma popisuje, jak nastavit stavy funkčních míst a modely životního cyklu v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16fbef7b390fd7a6c00bc5e4bdac28aee458613e4dc69941f26c7f7732e58de0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739172"
---
# <a name="functional-location-lifecycle-states"></a>Stavy životního cyklu funkčních míst

[!include [banner](../../includes/banner.md)]

 

Toto téma popisuje, jak nastavit stavy životního cyklu funkčních míst a modely životního cyklu v modulu Správa majetku. Stavy životního cyklu funkčního místa definují stavy, ve kterých může být funkční místo, například vytvořeno, aktivní a ukončeno. Všechna funkční místa, bez ohledu na jejich stav životního cyklu, můžete zobrazit na stránce se seznamem **Všechna funkční místa**. Stav funkčního místa můžete změnit tak, že ho vyberete na stránce se seznamem **Všechna funkční místa** a vyberete možnost **Aktualizovat stav funkčního místa**.

## <a name="set-up-functional-location-lifecycle-states"></a>Nastavení stavů životního cyklu funkčního místa

1. Zvolte **Správa majetku** > **Nastavení** > **Funkční místa** > **Stavy životního cyklu**.
2. Zvolte **Nový** pro vytvoření nového stavu funkčního místa.
3. Vložte ID stavu do pole **Stav životního cyklu** a název stavu funkčního místa v poli **Název**. V poli **Modely životního cyklu** se zobrazí počet modelů životního cyklu funkčních míst, které používají stav funkčních míst.
4. Na záložce s náhledem **Obecné** vyberte na přepínacím tlačítku **Aktivní** možnost Ano, pokud má být funkční místo v tomto stavu aktivní.
5. Na přepínacích tlačítku **Vytvořit majetek** vyberte možnost Ano, pokud má být možné automaticky vytvořit majetek se stejným názvem jako funkční místo a nainstalovat ho do funkčního místa v tomto stavu.  
>[!NOTE]
>Toto přepínací tlačítko se vztahuje k poli **Typ majetku** na záložce s náhledem **Obecné** ve formuláři **Typy funkčních míst** (**Správa majetku** > **Nastavení** > **Funkční místa** > **Typy funkčních míst**).
6. V případě, že má být možné změnit název funkčního místa v tomto stavu, na přepínacím tlačítku **Přejmenovat místo** zvolte Ano.
7. V případě, že má být možné přidat nová dílčí místa do funkčního místa v tomto stavu, na přepínacím tlačítku **Nová dílčí místa** zvolte Ano.
8. V případě, že má být možné instalovat majetky na funkčního místa v tomto stavu, na přepínacím tlačítku **Instalovat majetek** zvolte Ano.
9. V případě, že má být možné odstranit funkční místa v tomto stavu, na přepínacím tlačítku **Odstranit funkční místa** zvolte Ano.
10. Pokud chcete, aby byl stav životního cyklu majetku pro všechny majetky nainstalované na funkčním místě automaticky aktualizován v tomto stavu, vyberte stav majetku v poli **Stav životního cyklu**. Příklad: Pokud uzavřete funkční místo a nastavíte stav životního cyklu funkčního místa na Ukončeno, budete pravděpodobně chtít automaticky změnit stav životního cyklu majetku nainstalovaného v tomto funkčním místě na Nepoužívá se.


>[!NOTE]
>Stavy životního cyklu funkčních míst, modely životního cyklu a typy jsou propojeny a používány stejným způsobem jako stavy životního cyklu pracovních příkazů, modely životního cyklu pracovních příkazů a typy pracovních příkazů. 

## <a name="set-up-functional-location-lifecycle-models"></a>Nastavení modelů životního cyklu funkčního místa

Pokud jste vytvořili stavy životního cyklu vyžadované pro vaše funkční místa, lze je rozdělit do skupin. To se provádí za účelem vytvoření toku modelu životního cyklu, který lze použít pro různé typy funkčních míst. Je třeba vytvořit minimálně jeden standardní model životního cyklu funkčního místa.

1. Zvolte **Správa majetku** > **Nastavení** > **Funkční místa** > **Modely životního cyklu**.
2. Zvolte **Nový** pro vytvoření nového modelu životního cyklu.
3. Vložte ID modelu životního cyklu do pole **Model životního cyklu** a název modelu životního cyklu v poli **Název**. V polích **Typy funkčních míst** a **Stavy životního cyklu** se zobrazí počet typů funkčních míst, které používají model životního cyklu, a počet stavů vybraných v modelu životního cyklu.
4. Na záložce s náhledem **Stavy životního cyklu** vyberte stavy, které si přejete zahrnout v modelu. To se provádí kliknutím na stav v části **Zbývající stavy životního cyklu** a kliknutím na tlačítko se ![šipkou vpřed.](media/02-setup-for-functional-locations.png) .
5. Chcete-li pro model vybrat všechny dostupné stavy, klikněte na tlačítko ![vybrat všechny dostupné fáze](media/03-setup-for-functional-locations.png) . Všechny stavy jsou převedeny do části **Vybrané stavy životního cyklu**.
6. Chcete-li z modelu odebrat vybraný stav, vyberte stav v části **Vybrané stavy životního cyklu** a poté zvolte tlačítko se ![šipkou zpět](media/04-setup-for-functional-locations.png) .
7. Vyberte **Aktualizace stavu životního cyklu**, chcete-li definovat stavy životního cyklu, které mohou následovat po vybraném stavu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]