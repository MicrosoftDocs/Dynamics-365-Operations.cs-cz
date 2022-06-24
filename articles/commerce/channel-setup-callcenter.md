---
title: Nastavení kanálu kontaktního střediska
description: Tento článek popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 03/13/2020
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
ms.openlocfilehash: 219c84eb9a8c3b53467ed48c13775106c82dac63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864948"
---
# <a name="set-up-a-call-center-channel"></a>Nastavení kanálu kontaktního střediska


[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit kanálu kontaktního střediska v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled


V aplikaci Dynamics 365 Commerce je kontaktní středisko typem kanálu Commerce, který lze definovat v aplikaci. Definování kanálu pro entity kontaktního střediska umožňuje systému zařadit specifická data a zpracovat výchozí hodnoty do prodejních objednávek. Zatímco společnost může definovat více kanálů kontaktních center ve službě Commerce, je důležité si uvědomit, že jednotliví uživatelé mohou být spojeni pouze s jedním kanálem kontaktního centra. 

Před vytvořením nového kanálu kontaktního centra se ujistěte, že jste splnili [Požadavky pro zřízení kanálů](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Vytvořit a konfigurovat nový kanál kontaktního střediska

Chcete-li vytvořit a konfigurovat nový kanál kontaktního střediska, postupujte dle těchto kroků.

1. V navigačním podokně přejděte na **Retail a Commerce \> Kanály \> Kontaktní střediska \> Všechna kontaktních střediska**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název** zadejte název nového kanálu.
1. Vyberte patřičnou **Právnickou osobu** z rozevírací nabídky.
1. Vyberte odpovídající umístění **Skladu** z rozevírací nabídky. Toto místo bude použito jako výchozí v prodejních objednávkách vytvořených pro tento kanál kontaktního centra, pokud nebyla na úrovni odběratele nebo položky definována jiná výchozí nastavení.
1. Do pole **Výchozí odběratel** zadejte platného výchozího odběratele. Tato data slouží k pomoci při vytváření nových záznamů odběratelů při automatickém vyplňování výchozího nastavení. Při vytváření objednávek kontaktních středisek není vhodné vytvářet objednávky pro výchozího odběratele.
1. V poli **Profil oznámení e-mailem** zadejte platný profil e-mailového oznámení. Při vytváření a zpracování objednávek kontaktních středisek se pomocí profilu e-mailového oznámení spouští automatické e-mailové výstrahy pro zákazníky s informacemi o stavu jejich objednávky.
1. Zadejte informační kód **Přepisu ceny**. Je možné, že pro vás bude nutné vytvořit informační kód. Tento informační kód poskytuje sadu kódů důvodů, z nichž si uživatel bude při použití funkce přepsání ceny v objednávce kontaktního centra vycházet.
1. Zadejte informační kód **Kód blokování**. Je možné, že pro vás bude nutné vytvořit informační kód. Tento informační kód poskytuje sadu vlitelných kódů důvodů, z nichž si uživatel bude vybírat při odesílání blokované objednávky.
1. Zadejte informační kód **Kredit**. Je možné, že pro vás bude nutné vytvořit informační kód. Tento informační kód obsahuje sadu kódů důvodů, z nichž může uživatel vybírat při použití funkce kredit objednávek v centru volání k poskytování různých refundací odběrateli z důvodů služeb pro zákazníky.
1. Volitelné: nastavení finančních dimenzí na pevné záložce **Finanční dimenze**. Dimenze zadané v tomto poli budou výchozí pro každou prodejní objednávku vytvořenou v tomto kanálu kontaktního centra.
1. Klikněte na možnost **Uložit**.

V následujícím obrázku je znázorněno vytvoření nového kanálu kontaktního střediska.

![Nový kanál kontaktního střediska.](media/channel-setup-callcenter-1.png)

Následující obrázek znázorňuje příklad kanálu kontaktního centra.

![Příklad kanálu kontaktního střediska.](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Nastavení dodatečného kanálu

Další úkoly požadované pro nastavení kanálu kontaktního střediska zahrnují nastavení způsobů plateb a způsobů dodání.

Následující obrázek znázorňuje možnosti nastavení **Režimy dodávek** a **Způsobů platby** na kartě **Nastavení**.

![Další akce nastavení kanálu kontaktního střediska.](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Nastavení metod platby

Chcete-li nastavit metody platby pro každý typ platby podporovaný v tomto kanálu, postupujte takto. Uživatelé budou muset vybírat z předdefinovaných metod platby a propojit je s kanálem kontaktního střediska. Před nastavením metod platby na kontaktních střediscích nejprve nastavte hlavní metody platby v **Retail a Commerce \> Nastavení kanállu \> Metody platby \> Metody platby**.

1. V podokně akcí vyberte kartu **Nastavení** a poté vyberte možnost **Metody platby**.
1. V podokně akcí zvolte **Nový**.
1. V navigačním podokně vyberte způsob platby z dostupných předdefinovaných plateb.
1. Konfigurujte libovolná další nastavení, která jsou požadována pro typ platby. V případě kreditních karet, dárkových poukazů nebo věrnostních karet je vyžadována další instalace výběrem funkce **Nastavení karty**. 
1. Konfigurace správných účtů pro zaúčtování pro typ platby v části **Zaúčtování**.
1. V podokně akcí klikněte na možnost **Uložit**.

Na následujícím obrázku je znázorněn příklad hotovostní způsob platby.

![Příklad způsobů platby.](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Nastavit způsoby dodání

Nastavené způsoby dodání lze zobrazit výběrem **Způsobů dodání** z karty **Nastavení** v **Podokně akcí**.  

Chcete-li změnit nebo přidat způsob dodání, který má být přidružen k kanálu kontaktního střediska, postupujte podle následujících kroků.

1. Ve formuláři způsoby dodání na základě kontaktního střediska vyberte **Spravovat způsoby dodání**
1. V podokně akcí vyberte možnost **Nový** a vytvořte nový způsob dodání nebo vyberte existující režim.
1. V oddílu **Maloobchodní kanály** klikněte na **Přidat řádek**, chcete-li přidat kanál kontaktního centra. Přidání kanálů pomocí organizačních uzlů namísto přidání jednotlivých kanálů může zjednodušit přidávání kanálů.
1. Zajistěte, aby byl způsob dodání konfigurován daty na pevné záložce **Produkty** a **Adresy**. Nejsou-li pro způsob dodání platné žádné produkty nebo dodací adresy, při výběru objednávky dojde k chybám.
1. Po provedení změn v režimu kontaktní středisko pro konfiguraci dodání je nutné spustit úlohu **Zpracovat způsoby dodání** a rozbalit tak matici změn. Tato úloha se nachází v **Maloobchodní a velkoobchodní prodej \> IT pro maloobchod a velkoobchod \> Zpracovat způsoby dodání**.

Na následujícím obrázku je znázorněn příklad způsobu dodání.

![Nastavit způsoby dodání.](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Nastavení uživatele kanálu

Chcete-li vytvořit prodejní objednávku, která je propojena s kanálem kontaktního centra z programu Commerce Headquarters, musí být uživatel vytvářející prodejní objednávku propojen s kanálem kontaktního střediska. Uživatel nemůže ručně propojit prodejní objednávku vytvořenou v rámci služby Commerce Headquarters s kanálem kontaktního střediska. Odkaz je systematický a je založen na uživateli a vztahu uživatele k kanálu kontaktního střediska. Uživatel může být propojen pouze s jedním kanálem kontaktního centra.

1. V podokně akcí vyberte kartu **Kanál** a poté vyberte možnost **Uživatelé kanálu**.
1. V podokně akcí zvolte **Nový**.
1. Vyberte existující **ID uživatele** z rozevíracího seznamu výběrů, chcete-li tohoto uživatele propojit s kanálem kontaktního střediska

Po dokončení nastavení uživatele kanálu a uživatel vytvoří novou prodejní objednávku v Commerce Headquarters, bude prodejní objednávka propojena s přiřazeným kanálem kontaktního střediska. Všechny konfigurace tohoto kanálu budou systematicky použity pro prodejní objednávku. Uživatel může potvrdit, se kterým kanálem kontaktního střediska je prodejní objednávka propojena, a to zobrazením odkazu názvu kanálu v záhlaví prodejní objednávky.


### <a name="set-up-price-groups"></a>Nastavení cenových skupin

Cenové skupiny jsou volitelné, ale pokud jsou používány, mohou kontrolovat, které prodejní ceny budou nabídnuty odběratelům, kteří dodávají objednávky do kanálu kontaktního střediska. Pokud pro odběratele nebyla nakonfigurována cenová skupina nebo pokud nejsou použity cenové skupiny katalogu pro prodejní objednávku (pomocí pole **ID zdrojového kódu** v záhlaví objednávky kontaktního centra), použije se pro vyhledání cen položek Cenová skupina kanálů. Pokud v kanálu kontaktního střediska nebyla nalezena Cenová skupina, použijí se výchozí hlavní ceny zboží. 

Chcete-li nastavit cenovou skupinu, postupujte podle následujících pokynů.

1. V podokně akcí klikněte na kartu **Kanál** a poté vyberte možnost **Cenové skupiny**.
1. V podokně akcí klikněte na možnost **Nový**.
1. V rozevíracím seznamu vyberte **Maloobchodní cenovou skupinu**.

## <a name="additional-resources"></a>Další prostředky

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Funkce prodeje kontaktního střediska](call-center-functionality.md)

[Nastavení možností zpracování objednávky kontaktního střediska](set-up-order-processing-options.md)

[Katalogy kontaktního střediska](call-center-catalogs.md)

[Nastavení a práce s výstrahami u podvodů](set-up-fraud-alerts.md)

[Nastavení programů kontinuity pro kontaktní střediska](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]