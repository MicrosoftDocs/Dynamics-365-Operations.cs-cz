---
title: Modul vyhledávání objednávky
description: Toto téma popisuje modul vyhledání objednávky a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 0ae5c8a2eea84a9aa707f7c2f6f29950f2f48faa
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675110"
---
# <a name="order-lookup-module"></a>Modul vyhledávání objednávky

[!include [banner](includes/banner.md)]

Toto téma popisuje modul vyhledání objednávky a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.

Modul vyhledávání objednávek poskytuje formulář, který mohou zákazníci použít k vyhledání objednávek zadaných na webu elektronického obchodování. Používá se jako součást funkce [Povolit vyhledávání objednávek pro hostující pokladny](order-lookup-guest.md). Modul vyhledávání objednávek lze použít k vyhledání objednávek, které byly odeslány prostřednictvím webu elektronického obchodu, maloobchodního prodejního místa (POS) nebo call centra. Formulář může načíst objednávky, které byly odeslány jak hostujícími uživateli, tak registrovanými uživateli.

Následující obrázek ukazuje příklad formuláře, který je vykreslen modulem pro vyhledávání objednávek. Když zákazníci vyplní formulář a vyberou **Najít objednávku**, jsou přesměrováni na stránku s podrobnostmi objednávky.

![Formulář pro modul pro vyhledávání objednávek na stránce.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Vlastnosti modulu vyhledávání objednávky

| Název vlastnosti     | Hodnota     | popis |
|-------------------|-----------|-------------|
| Záhlaví           | Text      | Nadpis, který se zobrazí v horní části formuláře (například „Najděte svou objednávku“). |
| Formátovaný text         | Formátovaný text | Volitelný vysvětlující text, který se zobrazí pod nadpisem. |
| Typ stavu objednávky | Výčet      | <p>Vyberte typ informací, které bude formulář požadovat od zákazníka kromě ID potvrzení objednávky. V současné době jsou podporovány následující hodnoty:</p><ul><li><b>E-mail</b> - Formulář bude obsahovat pole, do kterého mohou zákazníci zadat e -mailovou adresu, kterou použili při zadávání objednávky.</li><li><b>Žádný</b> - Formulář nebude požadovat žádné informace kromě ID potvrzení objednávky.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Přidání modulu vyhledávacího kódu objednávky na stránku

Modul vyhledávání objednávek lze přidat do těla jakékoli stránky vašeho webu elektronického obchodování. Pokud chcete použít modul vyhledávání objednávek k povolení vyhledávání objednávek pro hostující pokladny, nezapomeňte ji přidat na stránku, která nevyžaduje přihlášení uživatele. Chcete-li najít nastavení **Vyžaduje přihlášení?** stránky ve stromovém zobrazení nástroje Commerce Site Builder, vyberte slot **Výchozí stránka (povinné)** a podívejte se do spodní části pravého panelu.

## <a name="additional-resources"></a>Další prostředky

[Povolit vyhledávání objednávek pro hostující pokladny](order-lookup-guest.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
