---
title: Otevření adresy URL v POS
description: Tento článek poskytuje přehled vylepšení, která byla provedena v aplikaci Dynamics 365 Commerce ohledně funkce vyhledávání produktu a vyhledávání zákazníka.
author: ShalabhjainMSFT
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.custom: 141393
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ad82cf1039515e58d1717453ee3fb4e3dafd84fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276420"
---
# <a name="open-url-in-pos"></a>Otevření adresy URL v POS

[!include [banner](includes/banner.md)]

Tento článek popisuje konfiguraci tlačítka v pokladním místě Dynamics 365 Commerce pro otevření adresy URL. Tato funkce nevyžaduje přizpůsobení kódu a může ji konfigurovat kdokoliv, i bez role vývojáře. 

Tato funkce umožňuje konfiguraci tlačítka v POS pomocí návrháře mřížky tlačítek pro otevření URL adresy. To je v současné době podporováno v následujících konfiguracích:

- Otevření v novém okně.
- Otevření v rámci POS.
- Otevření nativní aplikace.

## <a name="open-in-new-window"></a>Otevřít v novém okně

Tato konfigurace určuje, zda má být otevřena adresa URL v novém okně nebo v rámci aplikace. Když je webová URL adresa nakonfigurována k otevření v rámci aplikace, postranní navigační panel a horní lišta pokladního místa jsou viditelné a dostupné pro interakci uživatele. Když je nakonfigurována k otevření v novém okně, URL adresa se otevře v novém okně aplikace na Modern POS pro Windows a na nové kartě prohlížeče ve všech ostatních klientech POS. Chcete-li to povolit, je nutné konfigurovat adresu URL s vybranou možností **Otevřít v novém okně**.

## <a name="open-within-pos"></a>Otevření v rámci POS

Otevření webové adresy URL v pokladním místě je momentálně podporováno pouze pro Modern POS v systému Windows. Na dalších klientech se tato funkce vyvíjí a je plánována pro vydání v budoucích aktualizacích. Chcete-li to povolit, je nutné konfigurovat adresu URL s nevybranou možností **Otevřít v novém okně**.

## <a name="open-a-native-app"></a>Otevření nativní aplikace

Tato funkce také umožňuje zadat newebovou adresu URL pro otevření nativní aplikace. Můžete například určit URL protokoly, např. MailTo, SIP, IM nebo MSTEAMS, které lze pak zpracovat pomocí příslušných nativní aplikací na zařízení hostitele. Chcete-li to povolit, je nutné konfigurovat adresu URL s vybranou možností **Otevřít v novém okně**.

- U počítačů se systémem Windows nahlédněte do části [Export nebo import výchozích přidružení aplikace](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) a nastavte výchozí přidružení protokolu, pokud nastavujete svůj počítač pomocí Deployment Image Servicing and Management (DISM).
- Pokud používáte MDM, jako je například Intune, pro správu počítačů Windows, nahlédněte do [Zásady zprostředkovatele kryptografických služeb - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Pokud jste vývojář vytvářející vlastní web, nahlédněte do tématu [Spuštění výchozí aplikace pro identifikátor URI](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Snadné otevření nativní aplikace

Windows, iOS a Android povolují snadnější otevření aplikací, na základě přidružení protokolu aplikace. Pokud vaše aplikace není již nakonfigurována k tomu, aby zvládla otevírání z webového prohlížeče, budete možná potřebovat pro tuto konfiguraci vývojáře.

- Pro systém Windows nahlédněte do části [Povolení aplikací pro weby s použitím obslužných rutin URI aplikace](/windows/uwp/launch-resume/web-to-app-linking).
- U systému iOS nahlédněte do tématu [Univerzální odkazy pro vývojáře](https://developer.apple.com/ios/universal-links/).
- U systému Android nahlédněte do části [Zpracování odkazů aplikace Android](https://developer.android.com/training/app-links/).

| Klient                | Otevřít v novém okně | Otevření nativní aplikace | Otevření v rámci POS | Podrobnosti                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Moderní POS na systému Windows | ✓\*                | ✓               | ✓              | \* Otevře se v novém okně Modern POS |
| Cloud POS             | ✓\*                | ✓               | X              | \* Otevře se na nové kartě prohlížeče        |
| Modern POS na iOS     | ✓\*                | ✓               | X              | \* Otevře se na nové kartě prohlížeče        |
| Modern POS na systému Android | ✓\*                | ✓               | X              | \* Otevře se na nové kartě prohlížeče        |

## <a name="before-you-begin"></a>Než začnete

Než začnete, zkontrolujte způsob konfigurace v části [Rozvržení obrazovky pro pokladní místo](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>Otevření URL adresy v POS

Chcete-li nakonfigurovat, aby se URL adresa otevřela v pokladním místě, proveďte následující kroky.

1. V ústředí přejděte na **Maloobchod a velkoobchod \> Nastavení kanálu \> Nastavení POS \> POS \> Rozložení obrazovky**.
2. Vyberte **Mřížky tlačítek \> Návrhář**.
3. Vytvořte nové tlačítko.
4. Vyberte vlastnosti **tlačítka**.
5. Vyberte **Otevřít adresu URL** jako akci.
6. Zadejte adresu URL, kterou chcete použít.
7. Nakonfigurujte, zda otevřít adresu URL v novém okně.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
