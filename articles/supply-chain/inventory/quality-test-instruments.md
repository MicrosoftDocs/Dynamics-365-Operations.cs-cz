---
title: Testovací přístroje pro řízení kvality
description: Toto téma popisuje, jak vytvořit testovací přístroje, které bude možné použít pro testy na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d80a4f784a43e0d83d1f5b42f6740ef6da3add1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565896"
---
# <a name="quality-management-test-instruments"></a>Testovací přístroje pro řízení kvality

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit testovací přístroje, které bude možné použít pro testy na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.

Použijte stránku **Testovací přístroje** pro definování a zobrazení podrobností o zařízeních, která se používají k provádění testů na objednávkách kvality. Testovací přístroje jsou volitelné. Mohou však pomoci dát pracovníkům kvality vědět, které zařízení nebo nástroj by měli použít k provedení konkrétního testu.

## <a name="test-instrument-example"></a>Příklad testovacího přístroje

Provádíte různé testy elektrických komponent. Některé testy se týkají napěťového výstupu komponent, jeden test jejich teploty a jeden test jejich hmotnosti. K provedení jednotlivých testů se používají různé nástroje, zařízení nebo vybavení. Například pro měření napětí se používá voltmetr, pro měření teploty teploměr a pro měření hmotnosti se používá váha. Každé z těchto zařízení můžete nakonfigurovat jako testovací přístroj a označit měrnou jednotku, ve které by měly být zaznamenány výsledky testu. Například výsledky z voltmetru se zaznamenávají ve voltech, výsledky z teploměru se zaznamenávají ve stupních Fahrenheita nebo stupňů Celsia a výsledky z váhy se zaznamenávají v librách nebo kilogramech.

## <a name="create-a-test-instrument"></a>Vytvoření testovacího přístroje

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testovací přístroje**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Testovací přístroj** – zadejte jedinečné ID nebo název testovacího přístroje.
    - **Popis** – zadejte podrobný popis testovacího přístroje.
    - **Jednotka** – vyberte jednotku, ve které přístroj měří výsledky. Pole **Přesnost** se nastaví automaticky na základě jednotky, kterou vyberete.

1. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky

- [Test správy kvality](quality-tests.md)
- [Testovací skupiny pro řízení kvality](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
