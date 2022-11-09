---
title: Modul vyhledávání objednávky
description: Tento článek popisuje modul vyhledání objednávky a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a891de4a1da6641a02b8316d16ac2e9a8180fac1
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734238"
---
# <a name="order-lookup-module"></a>Modul vyhledávání objednávky

[!include [banner](includes/banner.md)]

Tento článek popisuje modul vyhledání objednávky a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.

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


> [!NOTE]
> Chcete-li povolit funkci vyhledávání objednávek, ujistěte se, že je klíč **Nabídka** je povolen v části **Konfigurace licence** > **Konfigurační klíče**.
>
> ![Musí být povolena konfigurace licenčního klíče nabídek](./media/Quotations_License_Key_Configuration.png)

## <a name="additional-resources"></a>Další prostředky

[Povolit vyhledávání objednávek pro hostující pokladny](order-lookup-guest.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
