---
title: Testovací proměnné správy kvality
description: Toto téma popisuje, jak vytvořit testovací proměnné, které bude možné použít pro testy kvality na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956579"
---
# <a name="quality-management-test-variables"></a>Testovací proměnné správy kvality

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit testovací proměnné, které bude možné použít pro testy kvality na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.

Pro každý test kvality definovaný na stránce **Testy** musíte definovat testovací proměnnou a její možné výstupy (výsledky). (U testů kvality je nutné v poli **Typ** stránce **Testy** nastavit hodnotu *Možnost*.)

Stránku **Testovací proměnné** použijte k nastavení, úpravě nebo zobrazení možných výsledků pro testovací proměnnou, která je přidružena k testu kvality. Každému výsledku přiřadíte stav výsledku *Úspěšné* nebo *Neúspěšné* k označení, zda je test úspěšný nebo neúspěšný, když je daný výsledek vybrán jako výsledek testu. Stránku **Testovací skupiny** použijte k přiřazení testovací proměnné a výchozího výsledku k jednotlivému testu kvality.

Pro každou testovací proměnnou doporučujeme definovat alespoň dva výsledky: jeden, který má stav výsledku *Úspěšné* a ten, který má stav výsledku *Neúspěšné*. Celkový počet proměnných nebo výsledků, které lze definovat, není nijak omezen. Několik testů může navíc k zaznamenávání výsledků používat stejné testovací proměnné.

## <a name="examples-of-test-variables"></a>Příklady testovacích proměnných

### <a name="example-1"></a>Příklad 1

Výrobní společnost provádí dva testy na vyráběných materiálech. V jednom testu je hladina pH přiřazena k barevnému pruhu. Přijatelné úrovně pH jsou ve světlejších barvách a nepřijatelné úrovně pH jsou v tmavších barvách. V jiném testu se provádí několik vizuálních kontrol a pracovníci v oblasti kvality pomocí svého úsudku určují, zda položka vizuální kontrole vyhovuje nebo zda neprochází.

### <a name="example-2"></a>Příklad 2

Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky. Kontrolní test má několik proměnných. Jedna proměnná odpovídá chuti, přičemž možné výsledky pro tuto proměnnou jsou „dobrá“ a „špatná“. Druhá proměnná odpovídá barvě, přičemž možné výsledky jsou „příliš tmavá“, „příliš světlá“ a „správná“.

## <a name="create-a-test-variable"></a>Vytvoření testovací proměnné

Pokud chcete vytvořit testovací proměnnou, postupujte takto.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testovací proměnné**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Proměnná** – zadejte jedinečné ID nebo název proměnné.
    - **Popis** – zadejte podrobný popis proměnné.

1. Zatímco je stále vybrán nový řádek, vyberte v podokně akcí možnost **Výsledky**.
1. Na stránce **Výsledky testovacích proměnných** vyberte v podokně akcí možnost **Nový**, a přidejte tak řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Výsledek** – zadejte jedinečné ID nebo název výsledku.
    - **Popis** – zadejte podrobný popis výsledku.
    - **Stav výsledku** – vyberte buď hodnotu *Úspěšné*, nebo *Neúspěšné* k označení, zda je test úspěšný nebo neúspěšný, když je daný výsledek vybrán jako výsledek testu.

1. Opakujte předchozí krok pro každý další výsledek. Ujistěte se, že alespoň jeden výsledek má stav výsledku *Úspěšné* a alespoň jeden má stav výsledku *Neúspěšné*.
1. Zavřete stránky.

## <a name="additional-resources"></a>Další prostředky

- [Testovací nástroje pro řízení kvality](quality-test-instruments.md)
- [Testy správy kvality](quality-tests.md)
- [Testovací skupiny pro řízení kvality](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
