---
title: Víceúrovňový majetek
description: Toto téma vysvětluje, jak vytvořit a odstranit víceúrovňové majetky.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a69fd8b7d81700a62ae96d679372b1d6c8a70bbf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253199"
---
# <a name="multi-level-assets"></a>Víceúrovňový majetek

[!include [banner](../../includes/banner.md)]

 

Toto téma vysvětluje, jak vytvořit a odstranit víceúrovňové majetky. Majetek a související dílčí majetek můžete vytvořit v hierarchické stromové struktuře. Tímto způsobem můžete znázornit vztahy a závislosti mezi majetky. Úlohy údržby mohou souviset se všemi úrovněmi stromové struktury. Statistiky lze vytvořit také pro jednotlivou úroveň nebo jako součet všech úrovní dílčích majetků.

Na stránce se seznamem **Všechen majetek** (**Správa majetku** \> **Obecné** \> **Majetek** \> **Všechen majetek**), sloupec **Majetek** zobrazuje seznam majetku v hierarchickém pořadí. Sloupec **Nadřazený** zobrazuje související nadřazený majetek. Pokud již byl majetek a dílčí majetek vytvořen, zobrazí se v části **Strom majetku** v podokně **Související informace** majetek ve stromové struktuře.

Informace o způsobu vytvoření majetku naleznete v tématu [Vytvoření majetku](../objects/create-an-object.md). Chcete-li vytvořit dílčí majetek, vyberte nadřazený majetek v poli **Nadřazený** na záložce s náhledem **Obecné**.

## <a name="copy-an-asset-or-asset-structure"></a>Kopírování majetku nebo struktury majetku

Pokud má vaše společnost několik podobných struktur majetku, můžete je rychle vytvořit pomocí funkce Kopírovat ve správě majetku.

1. Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek**.
2. Na stránce se seznamem **Všechen majetek** vyberte majetek, který chcete kopírovat. Chcete-li například zkopírovat celou strukturu majetku včetně dílčích majetků, vyberte nadřazený majetek.
3. Vyberte **Kopírovat majetek**. V části **Kopírovat z** je pole **Majetek** nastaveno na majetek, který jste vybrali na stránce se seznamem.
4. V části **Kopírovat do** zadejte do pole **Majetek** název nového majetku.
5. Pokud má být vytvářený majetek součástí existující struktury majetku, vyberte v části **Nadřazený majetek** v poli **Majetek** ID nadřazeného majetku.
6. Vyberte **OK**. Nová struktura majetku je zobrazena na stránce seznam **Všechen majetek**. Všechny atributy majetku, plány údržby a pořadí údržby související s majetkem, který jste zkopírovali, budou převedeny do nového majetku nebo struktury majetku.

Při kopírování struktury majetku mají dílčí majetky v nové struktuře stejný název jako dílčí majetky, které jste zkopírovali. Po dokončení procesu kopírování můžete snadno změnit název a další nastavení majetku. Vyberte majetek na stránce se seznamem **Všechen majetek** a zvolte tlačítko **Upravit**.

> [!NOTE]
> Když kopírujete majetek nebo strukturu majetku, stav životního cyklu nového majetku se obnoví do stavu, který jste definovali jako počáteční stav životního cyklu pro majetek. Funkční místo je resetováno na výchozí funkční místo.

## <a name="delete-an-asset-or-asset-structure"></a>Odstranění majetku nebo struktury majetku

Pokud má majetek související dílčí majetek, můžete jej odstranit pouze v případě, že na některém z těchto majetků nejsou registrovány žádné požadavky na údržbu, úlohy pracovního příkazu, chybné registrace nebo vyhodnocení podmínek.

1. Na stránce se seznamem **Všechen majetek** vyberte majetek, který chcete odstranit.
2. Zvolte **Odstranit**.

> [!NOTE]
> Pokud nemůžete odstranit majetek pomocí tohoto postupu, dalším způsobem odstranění je nastavení stavu životního cyklu majetku pro tento účel. Můžete například nastavit stav životního cyklu **Zlikvidováno** nebo **Odstraněno** na stránce **Stavy životního cyklu majetku**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]