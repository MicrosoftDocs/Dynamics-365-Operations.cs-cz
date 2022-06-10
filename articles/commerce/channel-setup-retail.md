---
title: Nastavení maloobchodního kanálu
description: Toto téma popisuje, jak vytvořit nový maloobchodní kanál v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 74a4f0f61e0bbfd73d0006d3cf45863af6fef18f
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770214"
---
# <a name="set-up-a-retail-channel"></a>Nastavení maloobchodního kanálu

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit nový maloobchodní kanál v řešení Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce podporuje více maloobchodních sítí. Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody). Každý kanál maloobchodu může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance. Všechny tyto prvky je třeba nastavit pro maloobchod před vytvořením kanálu maloobchodu. 

Před vytvořením maloobchodního kanálu se ujistěte, že splňujete [předpoklady kanálu](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Vytvořit a konfigurovat nový maloobchodní kanál

1. V navigačním podokně přejděte na **Moduly \> Kanály \> Obchody \> Všechny obchody**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název** zadejte název nového kanálu.
1. V poli **Číslo obchodu** zadejte jedinečné číslo obchodu. Číslo může být alfanumerické s maximálně 10 znaky.
1. V rozevíracím seznamu **Právnícká osoba** zadejte příslušnou právnickou osobu.
1. Do rozevíracího seznamu **Sklad** zadejte příslušný sklad.
1. V poli **Uložené časové pásmo** vyberte příslušné časové pásmo.
1. V rozevíracím seznamu **Skupina DPH** vyberte pro obchod příslušnou skupinu DPH.
1. V poli **Měna** vyberte příslušnou měnu.
1. V poli **Adresář odběratele** zadejte platný adresář.
1. Do pole **Výchozí odběratel** zadejte platného výchozího odběratele.
1. V poli **Funkční profil** vyberte funkční profil, pokud je k dispozici.
1. V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení.
1. V podokně akcí vyberte **Uložit**.

V následujícím obrázku je znázorněno vytvoření nového maloobchodního kanálu.

![Nový maloobchodní kanál.](media/channel-setup-retail-1.png)

Následující obrázek znázorňuje příklad maloobchodního kanálu.

![Příklad maloobchodního kanálu.](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Další nastavení

Existuje řada dalších volitelných nastavení, která lze nastavit v sekcích **Výkaz/uzávěrka** a **Různé** podle potřeb maloobchodního obchodu.

Kromě toho viz [Rozložení obrazovky pokladního místa (POS)](pos-screen-layouts.md) pro informace o nastavení výchozího rozvržení obrazovky v části **Rozložení obrazovky** a [Konfigurace a instalace Retail Hardware Station](retail-hardware-station-configuration-installation.md) pro informace o nastavení v části **Hardwarové stanice**.

Následující obrázek znázorňuje příklad konfigurace nastavení maloobchodního kanálu.

![Příklad konfigurace maloobchodní sítě.](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Nastavení dodatečného kanálu

Existují další položky, které je třeba nastavit pro kanál, který lze najít v podokně Akce v sekci **Nastavení**.

Další úkoly požadované pro nastavení online kanálu zahrnují nastavení způsobů plateb, výkazu hotovosti, způsobů dodání, účtu příjmů/výdajů a přiřazení skupiny plnění a trezorů.

Následující obrázek ukazuje další možnosti nastavení maloobchodních kanálů na kartě **Nastavení**.

![Nastavení kanálu.](media/channel-setup-retail-4.png)

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

Následující obrázek ukazuje příklad způsobu platby v hotovosti a konfiguraci karty **Množství**.

![Příklad nastavení způsobu platby pro částky.](media/payment-methods-recount.png)

> [!NOTE]
> Hodnoty pro kartu **Množství** jsou uloženy v mezipaměti na Retail Serveru a neprojeví se okamžitě po spuštění úloh plánu distribuce. Možná budete muset restartovat Cloud Scale Unit, abyste mohli tyto hodnoty okamžitě použít pro testování.

### <a name="set-up-cash-declaration"></a>Nastavení výkazu hotovosti

1. V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Výkaz hotovosti**.
1. V podokně akcí vyberte **Nový** a poté vytvořte všechny použitelné nominální hodnoty pro **Mince** a **Bankovky**.

Na následujícím obrázku je znázorněn příklad výkazu hotovosti.

![Nastavení výkazu hotovosti.](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Nastavit způsoby dodání

Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v Podokně akcí.  

Chcete-li změnit nebo přidat způsob dodání, postupujte podle následujících kroků.

1. V navigačním podokně přejděte na **Moduly \> Řízení zásob \> Způsoby dodání**.
1. V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.
1. V oddílu **Maloobchodní kanály** vyberte možnost **Přidat řádek**, chcete-li přidat kanál. Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.

Na následujícím obrázku je znázorněn příklad způsobu dodání.

![Nastavit způsoby dodání.](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Nastavit účet příjmů/výdajů

Chcete-li nastavit účet příjmů/výdajů, postupujte následujícím způsobem.

1. V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Účet příjmů/výdajů**.
1. V podokně akcí zvolte **Nový**.
1. V položce **Název** zadejte název.
1. V položce **Vyhledat název** zadejte název pro vyhledání.
1. V položce **Typ účtu** zadejte typ účtu.
1. V případě potřeby zadejte text pro **Řádek zprávy 1**, **Řádek zprávy 2**, **Text stvrzenky 1** a **Text stvrzenky 2**.
1. V položce **Zaúčtování** zadejte informace o zaúčtování.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad účtu příjmů/výdajů.

![Nastavit účty příjmů/výdajů.](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Nastavení sekcí

Chcete-li nastavit sekce, postupujte následujícím způsobem.

1. V podokně akcí vyberte kartu **Nastavení** a poté klikněte na možnost **Sekce**.
1. V podokně akcí zvolte **Nový**.
1. V položce **Číslo sekce** zadejte číslo sekce.
1. V položce **Popis** zadejte popis.
1. V položce **Velikost sekce** zadejte velikost sekce.
1. Konfigurujte další nastavení pro **Obecné** a **Prodejní statistiky** podle potřeby.
1. V podokně akcí vyberte **Uložit**.

### <a name="set-up-a-fulfillment-group-assignment"></a>Nastavení přiřazení skupiny plnění

Chcete-li nastavit přiřazení skupiny plnění, postupujte podle následujících pokynů.

1. V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.
1. V podokně akcí zvolte **Nový**.
1. V rozevíracím seznamu **Skupina plnění** vyberte skupinu plnění.
1. V rozevíracím sezamu **Popis** zadejte popis.
1. V podokně akcí vyberte **Uložit**

Následující obrázek znázorňuje příklad nastavení přiřazení skupiny plnění.

![Nastavení Přiřazení skupiny plnění.](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Nastavit trezory

Chcete-li nastavit trezory, postupujte následujícím způsobem.

1. V podokně akcí vyberte kartu **Nastavení** a poté klikněte na možnost **Trezory**.
1. V podokně akcí zvolte **Nový**.
1. Zadejte název trezoru.
1. V podokně akcí vyberte **Uložit**.

### <a name="ensure-unique-transaction-ids"></a>Zajištění jedinečných ID transakce

Počínaje verzí Commerce 10.0.18 jsou ID transakcí generovaná pro prodejní místo (POS) sekvenčně a zahrnují následující části:

- Pevná část, což je zřetězení ID obchodu a ID terminálu. 
- Sekvenční část, což je číselná řada. 

Konkrétně jde o formát *{store}-{terminal}-{numbersequence}*. 

Protože ID transakcí lze generovat v offline a online režimu, došlo k generování duplicitních ID transakcí. Eliminace duplicitních ID transakcí vyžaduje mnoho manuálního opravování dat. 

S verzí Commerce 10.0.19 byl aktualizován formát ID transakce, aby se odstranila sekvenční část, a místo toho se používá 13místné číslo generované výpočtem času v milisekundách od roku 1970. S touto změnou je nový formát ID transakce *{store}-{terminal}-{millisecondsSince1970}*. Tato aktualizace dělá ID transakce nesekvenční a zajišťuje, že ID transakcí jsou vždy jedinečná. 

> [!NOTE]
> Transakční ID jsou určena pouze pro interní použití systému, takže se nevyžaduje, aby byla sekvenční. Mnoho zemí však vyžaduje, aby identifikační čísla účtenek byla sekvenční.

Novou funkci formátu ID transakce lze povolit z pracovního prostoru **Správa funkcí**. 

Chcete-li povolit použití nových ID transakcí, postupujte takto:

1. V centru Commerce přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. Filtrujte modul „retail a commerce“.
1. Vyhledejte název funkce **Aktivovat nové ID transakce, aby se zabránilo duplicitním ID transakcí**.
1. Vyberte funkci a poté v pravém podokně vyberte možnost **Povolit nyní**.  
1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. Spusťte úlohy **Konfigurace kanálu 1070** a **Záznamník úloh 1170 POS** k synchronizaci povolené funkce s obchody.
1. Po odeslání změn do obchodů musí být POS terminály uzavřeny a znovu otevřeny, aby bylo možné použít nový formát ID transakce. 

> [!NOTE]
> Jakmile bude povolena nová funkce formátu ID transakce, nebudete ji moci deaktivovat. Pokud je třeba ji deaktivovat, kontaktujte podporu Commerce.

## <a name="additional-resources"></a>Další prostředky

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Nastavení online kanálu](channel-setup-online.md)

[Nastavení kanálu kontaktního střediska](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
