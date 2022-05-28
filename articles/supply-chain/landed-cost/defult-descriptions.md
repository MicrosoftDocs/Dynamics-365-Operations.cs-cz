---
title: Výchozí popisy pro hlavní knihu
description: Výchozí popisy lze použít k aktualizaci pole Popis v zaúčtování dokladů do hlavní knihy.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f95dff3a77a552d5788d813b3d13dc30579be715
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695700"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Výchozí popisy pro hlavní knihu

[!include [banner](../../includes/banner.md)]

Výchozí popisy lze použít k aktualizaci pole **Popis** v zaúčtování dokladů do hlavní knihy. Tato funkce byla vylepšena pro práci s náklady za doručení.

Chcete-li nastavit výchozí popisy zaúčtování do hlavní knihy, přejděte na uzel **Organizační správa \> Nastavení \> Výchozí popisy**.

V následující tabulce jsou uvedeny nové hodnoty, které byly přidány pro pole **Popis** na stránce **Výchozí popisy**, aby podporovaly náklady za doručení.

| Typ popisu | Poznámky |
|---|---|
| Importovat výpočet nákladů - časové rozlišení nákladů | Když je zaúčtována faktura za nákupní objednávku, je zpracováno časové rozlišení nákladů pro odhad nákladů na cestu. Lze zadat výchozí popisy, které do popisu přidají číslo cesty. Pro číslo dodávky použijte zápis *%4*. |
| Importovat výpočet nákladů – objednávka přepravovaného zboží | Pokud používáte zpracování během přepravy, zaúčtuje se faktura za nákupní objednávku a zboží se zaúčtuje na účet zboží v přepravě. Lze zadat výchozí popisy, které do popisu přidají číslo objednávky v přepravě. Pro číslo objednávky v přepravě použijte zápis *%4*. |
| Sklad – uzávěrka – úpravy | Když je faktura za závazky (AP) zpracována z hlediska nákladů na cestu, je zpracována úprava zásob pro odhad nákladů na cestu. Lze zadat výchozí popisy, které do popisu přidají číslo cesty. Pro číslo dodávky použijte zápis *%4*. |

Další informace o tom, jak pracovat se stránkou **Výchozí popisy** najdete v tématu [Nastavení výchozích popisů pro automatické zaúčtování](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
