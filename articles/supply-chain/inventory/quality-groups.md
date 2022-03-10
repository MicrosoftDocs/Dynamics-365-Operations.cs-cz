---
title: Skupiny kvality položek
description: Toto téma popisuje, jak použít a vytvořit skupiny kvality položek k logickému seskupení produktů tak, aby je bylo možné přiřadit k asociacím kvality pro automatické generování objednávek kvality.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f7a4932c561c052bec1eb0094a390e315b9b1bb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580905"
---
# <a name="item-quality-groups"></a>Skupiny kvality položek

[!include [banner](../includes/banner.md)]

Skupina kvality představuje společné požadavky na testování položek. Toto téma popisuje, jak použít a vytvořit skupiny kvality položek k logickému seskupení produktů tak, aby je bylo možné přiřadit k asociacím kvality pro automatické generování objednávek kvality.

K nastavení, úpravě a zobrazení položek zařazených do skupin kvality, které jsou přiřazeny položce přejděte do **Řízení zásob \> Nastavení \> Skupiny kvality**. Po určení požadavků na testování na stránce **Testovací skupiny** můžete definovat pravidla pro automatické generování objednávek kvality. Proces můžete zjednodušit tak, že nebudete definovat pravidla pro jednotlivé položky. Namísto toho můžete na stránce **Přidružení kvality** určít pravidla pro skupinu kvality.

## <a name="example-of-an-item-quality-group"></a>Příklad skupiny kvality zboží

Výrobní společnost nakupuje různé suroviny, které při vstupní kontrole podléhají stejným požadavkům na testování. Tak společnost definuje skupinu kvality a přiřadí čísla položek, které jsou přidruženy k surovinám, do této skupiny. Později společnosti zakoupí nový typ suroviny, který má stejné požadavky na testování. Namísto vytvoření nových požadavků na testování pro nový materiál společnost přidá číslo položky pro nový materiál do stávající skupiny kvality.

Stejná společnost vyrábí také položky, na které jsou kladeny stejné požadavky na testování, a expeduje položky, které před odesláním podléhají stejné kontrole. Tak společnost definuje další dvě skupiny kvality a do každé skupiny zařadí příslušné položky.

## <a name="create-a-quality-group"></a>Vytvoření skupiny kvality

Pokud chcete vytvořit skupinu kvality, postupujte takto.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Skupina kvality** - Zadejte jedinečné ID nebo název skupiny kvality.
    - **Popis** - Zadejte podrobný popis typu skupiny kvality.

1. Zavřete stránku.

## <a name="manually-add-items-to-a-quality-group"></a>Manuální přidání položek do skupiny kvality

Chcete-li ručně přidat položky do skupiny kvality, postupujte takto.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.
1. Vyberte skupinu kvality, do které chcete přidat položky.
1. V podokně akcí zvolte **Položky**.
1. Na stránce **Položky ve skupinách kvality** v podokně akcí vyberte **Nový** a přidejte řádek do mřížky. Poté pro nový řádek nastavte pole **Číslo položky** na číslo položky, kterou chcete přidat.
1. Opakujte předchozí krok pro každou další položku, kterou je třeba přidat.
1. Zavřete stránky.

## <a name="add-multiple-items-to-a-quality-group"></a>Přidání více položek do skupiny kvality

Chcete-li přidat více položek do skupiny kvality, postupujte takto.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.
1. Vytvořte nebo vyberte skupinu kvality, do které chcete přidat položky.
1. V podokně akcí zvolte **Přidat položky**.
1. V dialogovém okně **Poptávka** zadejte kritéria filtru pro položky, které chcete přidat. Můžete například filtrovat všechny položky v konkrétní skupině položek.
1. Vyberte **OK**.
1. V dialogovém okně **Přidání položek** mřížka zobrazuje všechny položky, které odpovídají vašemu dotazu. Zkontrolujte výsledky.

    Pokud jsou nutné nějaké změny, vyberte **Vybrat** pro návrat do dialogového okna **Poptávka** a upravte svůj dotaz.

1. Pokud výsledky zahrnují všechny položky, které chcete přidat, vyberte **OK**.
1. Zavřete stránku.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Ručně přidružte položku ke skupině kvality

Chcete-li ručně přidružit položku ke skupině kvality, postupujte takto.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality položek**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Číslo položky** - Vyberte číslo položky, kterou chcete přidat.
    - **Skupina kvality** - Vyberte skupinu kvality, kterou chcete přiřadit k položce.

1. Opakujte předchozí krok pro každou další kombinaci položky a skupiny kvality, které je třeba přidat.
1. Zavřete stránky.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Ručně přidejte skupinu kvality ze stránky Vydané produkty

Pro ruční přidání skupiny kvality ze stránky **Vydané produkty** postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt, ke kterému chcete přiřadit skupinu kvality.
1. V podokně Akce na kartě **Spravovat sklad** ve skupině **Kvalita** vyberte **Skupiny kvality položek**.
1. Na stránce **Položky ve skupinách kvality** v podokně akcí vyberte **Nový** a přidejte řádek do mřížky. Poté pro nový řádek nastavte pole **Skupina kvality** na skupinu kvality, kterou chcete produktu přiřadit.
1. Opakujte předchozí krok pro každou další skupinu kvality, kterou chcete produktu přiřadit.
1. Zavřete stránky.

## <a name="additional-resources"></a>Další prostředky

- [Testovací nástroje pro řízení kvality](quality-test-instruments.md)
- [Testy správy kvality](quality-tests.md)
- [Testovací skupiny pro řízení kvality](quality-test-groups.md)
- [Testovací proměnné pro řízení kvality](quality-test-variables.md)
- [Přiřazení kvality](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
