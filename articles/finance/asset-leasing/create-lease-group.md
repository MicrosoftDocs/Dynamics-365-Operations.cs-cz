---
title: Vytvoření skupiny leasingu
description: Tento článek vysvětluje, jak nastavit skupiny leasingu. Skupiny leasingu jsou nutné k vytvoření nových leasingů.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd1a6f61346233bf205657917c65fccd82167f7f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895015"
---
# <a name="create-a-lease-group"></a>Vytvoření skupiny leasingu

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit skupiny leasingu. Skupiny leasingu jsou nutné k vytvoření nových leasingů. Leasingové knihy jsou přidruženy ke každé skupině leasingu. Leasingové knihy určují výchozí knihy, které musí být vytvořeny pro každý leasing. Konkrétní účty můžete přiřadit skupině leasingu na stránce **Parametry zaúčtování leasingu**.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Vytvořte leasingovou knihu a přidejte skupinu leasingu

1. Přejděte na **Leasing majetku \> Nastavení \> Skupiny leasingu**.
2. V podokně Akce volbou **Nový** přidejte skupinu leasingu. Do mřížky je přidán řádek.
3. Na novém řádku v poli **Skupina leasingu** zadejte hodnotu.
4. V poli **Popis** zadejte hodnotu.

Informace, které jste právě zadali, se přidají do pole **Skupina leasingu** na stránce **Přidat leasing**.

## <a name="associate-a-book-with-a-lease-group"></a>Přidružení knihy ke skupině leasingu

Po vytvoření skupin leasingu můžete ke každé skupině přiřadit knihy. Když vytvoříte leasing a přiřadíte jej ke skupině leasingu, systém vytvoří sadu plánů pro každou knihu, která je přidružena k dané skupině leasingu.

> [!NOTE]
> Knihy je třeba vytvořit, než je lze přiřadit ke skupině leasingu.

1. Přejděte na **Leasing majetku \> Nastavení \> Skupina leasingu**.
2. Vyberte skupinu leasingu a poté vyberte **Knihy**.
3. Vyberte **Nový** a poté v poli **Typ knihy** vyberte knihu, kterou chcete přiřadit do skupiny leasingu. Skupině leasingu můžete přiřadit více knih, pokud musí být leasing účtován různými způsoby.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
