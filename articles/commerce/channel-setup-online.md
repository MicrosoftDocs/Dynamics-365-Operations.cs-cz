---
title: Nastavení online kanálu
description: Tento článek popisuje, jak vytvořit nový online kanál v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: be9fafe8ece771ad6577db1cdb70af6f48e054cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272873"
---
# <a name="set-up-an-online-channel"></a>Nastavení online kanálu

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit nový online kanál v řešení Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce podporuje více maloobchodních sítí. Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody). Online obchody nabízí zákazníkům možnost nákupu produktů prodejce online i v maloobchodě.

Chcete-li vytvořit online obchod v rámci služby Commerce, musíte nejprve vytvořit online kanál. Před vytvořením nového online kanálu se ujistěte, že jste splnili [Požadavky pro zřízení kanálů](channels-prerequisites.md).

Než bude možné vytvořit nový web, musí být v aplikaci Commerce vytvořen alespoň jeden online obchod. Další informace najdete v části [Vytvoření webu elektronického obchodu](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Vytvořit a konfigurovat nový online kanál

Chcete-li vytvořit a konfigurovat nový online kanál, postupujte dle těchto kroků.

1. V navigačním podokně přejděte na **Moduly \> Kanály \> Online obchody**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název** zadejte název nového kanálu.
1. V rozevíracím seznamu **Právnícká osoba** zadejte příslušnou právnickou osobu.
1. Do rozevíracího seznamu **Sklad** zadejte příslušný sklad.
1. V poli **Uložené časové pásmo** vyberte příslušné časové pásmo.
1. V poli **Měna** vyberte příslušnou měnu.
1. Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.
1. V poli **Adresář odběratele** zadejte platný adresář.
1. V poli **Funkční profil** vyberte funkční profil, pokud je k dispozici.
1. V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.
1. V podokně akcí vyberte **Uložit**.

V následujícím obrázku je znázorněno vytvoření nového online kanálu.

![Nvý online kanál.](media/channel-setup-online-1.png)

Následující obrázek znázorňuje příklad online kanálu.

![Příklad online kanálu.](media/channel-setup-online-2.png)

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>Přiřazení kanálu k Commerce Scale Unit

Váš nový kanál musí být přiřazen k Commerce Scale Unit. Pokyny viz [Konfigurace kanálů pro použití Commerce Scale Unit](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit).

## <a name="set-up-languages"></a>Nastavit jazyky

Pokud váš web e-Commerce bude podporovat více jazyků, rozbalte část **Jazyky** a podle potřeby přidejte další jazyky.

## <a name="set-up-payment-account"></a>Nastavit účet platby

V části **Platební účet** můžete přidat poskytovatele plateb třetí strany. Informace o nastavení platebního konektoru Adyen naleznete v tématu [Platební konektor Dynamics 365 pro Adyen](./dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Nastavení dodatečného kanálu

Další úkoly požadované pro nastavení online kanálu zahrnují nastavení způsobů plateb, způsobů dodání a přiřazení skupiny plnění.

Následující obrázek znázorňuje možnosti nastavení **Režimy dodávek**, **Způsobů platby** a **Přiřazení skupiny plnění** na kartě **Nastavení**.

![Další akce nastavení online kanálu.](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Nastavení metod platby

Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto.

1. V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.
1. V podokně akcí zvolte **Nový**.
1. V navigačním podokně vyberte požadovaný způsob platby.
1. V části **Obecné** zadejte **Název operace** a nakonfigurujte další požadovaná nastavení.
1. Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby.
1. V podokně akcí vyberte **Uložit**.

Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.

![Příklad způsobů platby.](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Nastavit způsoby dodání

Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.  

Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.

1. V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.
1. V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.
1. V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál. Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.

Na následujícím obrázku je znázorněn příklad způsobu dodání.

![Nastavit způsoby dodání.](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Nastavení přiřazení skupiny plnění

Chcete-li nastavit přiřazení skupiny plnění, postupujte podle následujících pokynů.

1. V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.
1. V podokně akcí zvolte **Nový**.
1. V rozevíracím seznamu **Skupina plnění** vyberte skupinu plnění.
1. V rozevíracím sezamu **Popis** zadejte popis.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad nastavení přiřazení skupiny plnění.

![Nastavení Přiřazení skupiny plnění.](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Nastavení maloobchodního kanálu](channel-setup-retail.md)

[Nastavení kanálu kontaktního střediska](channel-setup-callcenter.md)

[Platební konektor Dynamics 365 pro Adyen](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
