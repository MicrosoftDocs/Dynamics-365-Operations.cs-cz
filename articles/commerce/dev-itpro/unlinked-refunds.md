---
title: Zpracujte nepropojené refundace pomocí Dynamics 365 Commerce Payment Connector pro Adyen
description: Tento článek popisuje, jak fungují nepropojené refundace , když se používá Microsoft Dynamics 365 Payment Connector pro Adyen.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 2b2bee7ad45bbff82c8b7de2741925fde29d8583
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284304"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Zpracujte nepropojené refundace pomocí Dynamics 365 Commerce Payment Connector pro Adyen

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak fungují nepropojené refundace , když se používá [Microsoft Dynamics 365 Payment Connector pro Adyen](adyen-connector.md). Zkoumá také schopnost zpracovat refundaci za novou platební metodu v podkladním místě (POS) nebo call centru.

Dynamics 365 Payment Connector pro Adyen podporuje schopnost zpracovávat refundace pomocí jiné platební metody, než jaká byla použita pro původní transakci. Ačkoli doporučujeme používat [propojené refundace](linked-refunds.md) ke zpracování refundací oproti původní platební metodě, která byla poskytnuta, je v některých případech vyžadována refundace jiným způsobem. Například kartě, která byla použita k původní platbě, může nyní vypršet platnost nebo se ztratit, nebo ji mohl zrušit uživatel.

## <a name="prerequisites"></a>Předpoklady

Následující předpoklady musí být splněny, než může Dynamics 365 Payment Connector pro Adyen zpracovat nepropojené refundace:

- Nastavte [způsobů platby](../payment-methods.md).
- Nastavte [omnikanálové platby](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Další konfigurace

Konektor Dynamics 365 Payment Connector for Adyen poskytuje přednastavenou implementaci každého podporovaného scénáře refundace, který je popsán v následující části. Zákazníci, kteří nepoužívají přednastavenou implementaci Dynamics 365 Payment Connect pro Adyen, musí nastavit konektor, který podporuje tokenizaci kreditních karet.

## <a name="supported-refund-scenarios"></a>Podporované scénáře refundace

Dynamics 365 Commerce podporuje refundace transakcí, které byly dříve schváleny a potvrzeny. Refundace může zahrnovat buď úplné vrácení peněz, nebo částečné vrácení transakce. Refundace nesmí překročit celou částku původní platby. Nepropojené refundace jsou podporovány pouze v POS a call centru.

## <a name="enable-unlinked-refunds-functionality"></a>Povolit nepropojené funkce vracení peněz

Chcete-li aktivovat funkci nepropojených refundací v centrále Commerce, postupujte takto.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry obchodu**.
1. Na kartě **Omnikanálové platby** nastavte možnost **Použít omnikanálové platby** na **Ano**.

### <a name="supported-payment-method-variants"></a>Podporované varianty způsobu platbu

Následující varianty platebních metod podporují nepropojené refundace ve výchozím nastavení:

- Karty
- Peněženka

Ne všechny varianty platebních metod podporují nepropojené refundace. Následující tabulka obsahuje seznam běžných platebních metod a ukazuje možnosti podpory jednotlivých metod pro propojené a nepropojené refundace.

| Způsob platby        | Propojená refundace | Nepropojená refundace |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Ano           | Ano             |
| amexconsumer          | Ano           | Ano             |
| amexcorporate         | Ano           | Ano             |
| amexdebit             | Ano           | Ano             |
| amexprepaid           | Ano           | Ano             |
| amexprepaidreloadable | Ano           | Ano             |
| amexsmallbusiness     | Ano           | Ano             |
| discover              | Ano           | Ano             |
| maestro               | Ano           | Ano             |
| maestrouk             | Ano           | Ano             |
| mc                    | Ano           | Ano             |
| mcalphabankbonus      | Ano           | Ano             |
| mcprepaidanonymous    | Ano           | Ano             |
| visa                  | Ano           | Ano             |
| visaalphabankbonus    | Ano           | Ano             |
| visacheckout          | Ano           | Ano             |
| visadankort           | Ano           | Ano             |
| visahipotecario       | Ano           | Ano             |
| visasaraivacard       | Ano           | Ano             |
| vpay                  | Ano           | Ano             |
| givex                 | **Žádná**        | Ano             |
| svs                   | **Žádná**        | Ano             |
| cup                   | Ano           | Ano             |
| diners                | Ano           | Ano             |
| interac               | **Žádná**        | Ano             |
| jcb                   | Ano           | Ano             |
| jcb_applepay          | Ano           | Ano             |
| unionpay              | Ano           | Ano             |

### <a name="process-an-unlinked-refund-in-pos"></a>Zpracování nepropojené refundace v POS

Zákazník vrátí položku pokladníkovi POS v povolené lhůtě pro vrácení a má platný doklad. Během zpracování vrácení obsahuje dialogové okno **Vrácení platby** možnost **Vybrat způsob platby**. Pokladník pak může vybrat způsob platby mezi podporovanými platebními metodami pro vracení peněz (karty a peněženka).

### <a name="process-an-unlinked-refund-in-call-center"></a>Zpracování nepropojené refundace v call centru

Když je nepropojená refundace zpracována proti objednávce v call centru, zaměstnanec call centra zvolí platební metodu, která se liší od původní metody. Zaměstnanec je poté vyzván, aby získal přepsání osobního identifikačního čísla (PIN) správcem. PIN bude vyžadován před zpracováním jiné platební metody pro refundaci.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Nastavte PIN pro přepsání správce pro call centrum

Chcete-li nastavit PIN pro přepsání správce pro call centrum v centrále Commerce, postupujte takto.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení call centra** nebo vyhledejte „Přepsat oprávnění“.
1. Vyberte roli, pro kterou chcete povolit oprávnění ke zpracování nepropojené refundace.
1. Na pevné záložce **Vrácení** nastavte možnost **Povolit alternativní platbu** na hodnotu **Ano**.

## <a name="additional-resources"></a>Další prostředky

[Aplikace Dynamics 365 Payment Connector pro Adyen](adyen-connector.md)

[Propojené refundace dříve schválených a potvrzených transakcí](linked-refunds.md)
