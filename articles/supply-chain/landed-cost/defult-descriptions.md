---
title: Výchozí popisy pro hlavní knihu
description: Výchozí popisy lze použít k aktualizaci pole Popis v zaúčtování dokladů do hlavní knihy.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500373"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Výchozí popisy pro hlavní knihu

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Výchozí popisy lze použít k aktualizaci pole **Popis** v zaúčtování dokladů do hlavní knihy. Tato funkce byla vylepšena pro práci s náklady za doručení.

Chcete-li nastavit výchozí popisy zaúčtování do hlavní knihy, přejděte na uzel **Organizační správa \> Nastavení \> Výchozí popisy**.

V následující tabulce jsou uvedeny nové hodnoty, které byly přidány pro pole **Popis** na stránce **Výchozí popisy**, aby podporovaly náklady za doručení.

| Typ popisu | Poznámky |
|---|---|
| Importovat výpočet nákladů - časové rozlišení nákladů | Když je zaúčtována faktura za nákupní objednávku, je zpracováno časové rozlišení nákladů pro odhad nákladů na cestu. Lze zadat výchozí popisy, které do popisu přidají číslo cesty. Pro číslo dodávky použijte zápis *%4*. |
| Importovat výpočet nákladů – objednávka přepravovaného zboží | Pokud používáte zpracování během přepravy, zaúčtuje se faktura za nákupní objednávku a zboží se zaúčtuje na účet zboží v přepravě. Lze zadat výchozí popisy, které do popisu přidají číslo objednávky v přepravě. Pro číslo objednávky v přepravě použijte zápis *%4*. |
| Sklad – uzávěrka – úpravy | Když je faktura za závazky (AP) zpracována z hlediska nákladů na cestu, je zpracována úprava zásob pro odhad nákladů na cestu. Lze zadat výchozí popisy, které do popisu přidají číslo cesty. Pro číslo dodávky použijte zápis *%4*. |

Další informace o tom, jak pracovat se stránkou **Výchozí popisy** najdete v tématu [Nastavení výchozích popisů pro automatické zaúčtování](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
