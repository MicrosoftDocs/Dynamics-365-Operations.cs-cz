---
title: Proaktivní parametry chatu modulu Commerce Chat
description: Tento článek popisuje parametry proaktivního chatu modulů Commerce chat v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691048"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Proaktivní parametry chatu modulu Commerce Chat

[!include [banner](includes/banner.md)]

Tento článek popisuje parametry proaktivního chatu Commerce Chat s Omnikanálem pro Customer Service a Commerce Chat s Power Virtual Agents v Microsoft Dynamics 365 Commerce.

## <a name="proactive-chat-properties"></a>Vlastnosti proaktivního chatu

Vlastnosti proaktivního chatu se nacházejí v podokně vlastností obchodního chatu s Omnikanálem pro Customer Service a Commerce Chat s Power Virtual Agents v nástroji pro tvorbu webů Commerce.

> [!NOTE]
> Ve výchozím nastavení jsou všechny zde uvedené vlastnosti proaktivního chatu prázdné. Doporučujeme, abyste se o těchto vlastnostech dozvěděli více a nastavili je pouze tak, jak jsou vyžadovány. Tento přístup pomůže omezit spouštění chybných proaktivních chatů.

### <a name="proactive-chat"></a>Proaktivní chat

| Popisný název | Popis | Výchozí hodnota |
|---------------|-------------|---------------|
| Povoleno | Aktivně zapojte zákazníky na základě různých spouštěčů. | Zakázáno |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. | Bianko |

### <a name="wait-time-proactive-chat"></a>Doba čekání (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Čas čekání (sek) | Čas (v sekundách), který uživatelé webu stráví na stránce webu, než se spustí proaktivní chat. |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="number-of-page-visits-proactive-chat"></a>Počet návštěv stránky (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Počet návštěv stránky | Počet návštěv stránky před spuštěním proaktivního chatu. Uživatelé webu musí nejprve přijmout výzvu v banneru souhlasu se soubory cookie. |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="specific-pages-proactive-chat"></a>Konkrétní stránky (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Stránka(y) | Seznam stránek, které při návštěvě spustí proaktivní chat. |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="from-specific-pages-proactive-chat"></a>Od konkrétní stránky (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Stránka(y) | Seznam stránek, které při návštěvě spustí proaktivní chat, když z nich uživatelé odejdou. |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="specific-countryregion-proactive-chat"></a>Konkrétní země/oblast (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Kód země | Uživatelé, kteří navštíví zadané země nebo oblasti, spustí proaktivní chat. Kód země/oblasti by měl obsahovat dvě velká písmena (např. **US**). |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="date-range-proactive-chat"></a>Rozsah dat (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Datum zahájení (dd/mm/rrrr) | Datum, kdy nebo po kterém bude spuštěn proaktivní chat. |
| Datum ukončení (dd/mm/rrrr) | Datum, kdy nebo před kterým bude spuštěn proaktivní chat. |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="total-amount-in-cart-proactive-chat"></a>Celková částka v košíku (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Minimum | Minimální peněžní částka (včetně) v nákupním košíku, která spustí proaktivní chat, když uživatelé navštíví stránku košíku. |
| Maximum | Maximální peněžní částka (včetně) v nákupním košíku, která spustí proaktivní chat, když uživatelé navštíví stránku košíku. |
|Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Celkový počet položek v košíku (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| Minimum | Minimální počet položek (včetně) v nákupním košíku, která spustí proaktivní chat, když uživatelé navštíví stránku košíku. |
| Maximum | Maximální počet položek (včetně) v nákupním košíku, která spustí proaktivní chat, když uživatelé navštíví stránku košíku. |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

### <a name="specific-products-in-cart-proactive-chat"></a>Konkrétní produkty v košíku (proaktivní chat)

| Popisný název | Popis |
|---------------|-------------|
| ID/SKU produktu | Seznam ID produktů/čísla skladových jednotek (SKU), které spustí proaktivní chat, když uživatelé navštíví stránku košíku. |
| Chatovací pozdrav | Uvítací zpráva, která se používá, když byl spuštěn proaktivní chat. |

## <a name="additional-resources"></a>Další prostředky

[Přehled funkcí chatu Commerce](commerce-chat-overview.md)

[Commerce chat s modulem Omnikanál pro Customer Service](commerce-chat-module.md)

[Modul chatu Commerce s Power Virtual Agents](chat-module-pva.md)
