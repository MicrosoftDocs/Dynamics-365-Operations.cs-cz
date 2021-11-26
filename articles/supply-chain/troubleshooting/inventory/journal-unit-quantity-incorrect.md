---
title: Jednotka a množství jednotky nefungují v deníku zásob správně
description: Jednotka a množství jednotky nefungují v deníku zásob správně
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 074be71d7b6ec1acab6307a79e397c2a2a045c39
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778418"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Jednotka a množství jednotky nefungují v deníku zásob správně

## <a name="symptoms"></a>Příznaky

Při práci s jednotkami a množstvími v deníku zásob se můžete setkat s jedním nebo oběma z následujících problémů:

- Když je pro vydaný produkt nastavena jednotka převodu, nevidíte v deníku zásob jednotky ani množství jednotek a nemůžete jednotku v deníku zásob změnit.
- V deníku zásob vidíte pole **Množství** a **Jednotka**, ale nevidíte pole **množství jednotky**. Pokud změníte jednotku, zadejte množství a zaúčtujete deník, deník stále zobrazuje původní měrnou jednotku pro toto množství.

## <a name="resolution"></a>Řešení

Chcete-li opravit problém, postupujte následovně.

1. V pracovním prostoru **Správa funkcí** se ujistěte, že je zapnutá funkce *Použití měrné jednotky a jednotkového množství v denících zásob*. Tato funkce přidává pole **Jednotka** a **Jednotkové množství** do deníku. (Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta.)
1. Po zapnutí funkce použijte pole **Množství**, **Jednotkové množství**, a **Jednotka** následujícím způsobem:

    - **Množství** - Určete množství pomocí výchozí jednotky definované pro vydaný produkt. Samotná výchozí jednotka se zde však nezobrazuje. Pokud je nastaven převod mezi výchozí jednotkou a jednotkou vybranou v poli **Jednotka**, pole **Množství** se automaticky aktualizuje na základě výběrů v poli **Jednotkové množství** a v poli **Jednotka**.
    - **Jednotkové množství** – určete množství pro měrnou jednotku vybranou v poli **Jednotka**.
    - **Jednotka** - Vyberte jednotku, která se má použít pro hodnotu v poli **Jednotkové množství**.
