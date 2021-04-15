---
title: Vytvoření skupiny leasingu
description: Toto téma vysvětluje, jak nastavit skupiny leasingu. Skupiny leasingu jsou nutné k vytvoření nových leasingů.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5d5efb02c95d9368fbc178cfd9bcd7ce088d1c66
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816045"
---
# <a name="create-a-lease-group"></a>Vytvoření skupiny leasingu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit skupiny leasingu. Skupiny leasingu jsou nutné k vytvoření nových leasingů. Leasingové knihy jsou přidruženy ke každé skupině leasingu. Leasingové knihy určují výchozí knihy, které musí být vytvořeny pro každý leasing. Konkrétní účty můžete přiřadit skupině leasingu na stránce **Parametry zaúčtování leasingu**.

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