---
title: Nastavení webu elektronického obchodování B2B
description: Toto téma popisuje, jak nastavit web elektronického obchodování typu business-to-business (B2B) v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 171e518258e9600bd7526cf52e3e456d272e6bce
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891378"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>Vytvoření webu elektronického obchodu B2B

[!include [banner](../../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Weby elektronického obchodování typu business-to-business (B2B) poskytují některé klíčové funkce, které optimalizují pracovní postup pro uživatele B2B. Toto téma popisuje, jak nastavit web elektronického obchodování typu B2B v Microsoft Dynamics 365 Commerce. Prochází moduly a nastavením webů, které je nutné nakonfigurovat, aby se umožnily scénáře specifické pro B2B.

## <a name="prerequisites"></a>Předpoklady

- Chcete-li nastavit web B2B elektronického obchodování, musíte povolit a nakonfigurovat konkrétní funkce v centrále Commerce, jak je popsáno v tomto tématu.
- Základní prostředí, jako je objevování produktů, stránky s podrobnostmi o produktu, košík a pokladna, jsou poháněny stejnými moduly, které se používají pro weby elektronického obchodování business-to-consumer (B2C). Autoři stránek by měli být obeznámeni se všemi moduly, které Dynamics 365 Commerce podporuje. Další informace viz [Přehled knihoven modulů](../starter-kit-overview.md).
- Toto téma předpokládá, že autoři webů rozumějí základům konfigurátoru webů Commerce, šablon, fragmentů a stránek, aby mohli povolit funkce B2B pro weby elektronického obchodování.

## <a name="site-level-settings"></a>Nastavení na úrovni webu

Nastavení na úrovni webu najdete v konfigurátoru webů na adrese **Nastavení webu \> Rozšíření**. Pro scénáře B2B platí následující dvě nastavení na úrovni webu:

- **Povolit platby zákaznickým účtem** - Tato vlastnost umožňuje uživatelům platit za objednávky pomocí zákaznických účtů. Dostupné hodnoty jsou **Povoleno pro zákazníky B2B**, **Povoleno pro zákazníky B2C**, **Povoleno pro všechny zákazníky** a **Zakázáno pro všechny zákazníky**. Pokud váš web B2B podporuje zákaznické účty, měli byste vybrat **Povoleno pro zákazníky B2B**.
- **Povolit limity množství objednávky** - Tato vlastnost umožňuje nastavit limity počtu položek, které lze objednat pro každý produkt nebo kategorii. Dostupné hodnoty jsou **Povoleno pro zákazníky B2B**, **Povoleno pro zákazníky B2C**, **Povoleno pro všechny zákazníky** a **Zakázáno pro všechny zákazníky**.

> [!NOTE]
> Při upgradu na nejnovější verzi knihovny modulů musíte provést další kroky, abyste zajistili, že ve vašem prostředí bude k dispozici dříve popsané nastavení webu. Další informace viz [Aktualizujte soubor app.settings.json](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Vytvořte stránky pro přihlášení obchodního partnera

Aby se uživatelé stali obchodními partnery, musí nejprve odeslat žádost obchodního partnera. Na domovské stránce B2B bude k dispozici odkaz na stránku požadavku obchodního partnera, aby uživatelé mohli zahájit proces. Poté, co uživatelé odešlou požadavek obchodního partnera, obdrží potvrzení, že požadavek byl odeslán. 

### <a name="create-a-business-partner-request-page"></a>Vytvořte stránku požadavku obchodního partnera

Modul **Registrace partnerů** stránce požadavku obchodního partnera se používá k iniciování požadavků uživatelů, aby se stali obchodními partnery. Tento modul umožňuje shromažďovat informace o uživateli, které jsou vyžadovány pro proces registrace. Navíc, modul **Adresa obchodního účtu** slouží k zachycení adresy uživatele.

Chcete-li nastavit a nakonfigurovat stránku požadavku obchodního partnera v nástroji pro tvorbu webů, postupujte takto.

1. Vytvořte šablonu s názvem **Registrace**. Tato šablona by měla obsahovat následující moduly:

    - Registrace partnera
    - Popis cesty
    - Záhlaví
    - Zápatí
    - Blok obsahu
    - Blok textu
    - Kolekce produktů

1. Použijte šablonu **Registrace** k vytvoření stránky s názvem **Žádost obchodního partnera**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na domovskou stránku a zadejte **Domovská stránka** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **Registrace partnera** pod modul **Popis cesty**. V podokně vlastností modulu v částu **Nadpis** vložte **Staňte se obchodním partnerem**.
1. Do slotu **Registrace partnera** přidejte modul **Adresa obchodního účtu**.
1. Do slotu **Kontejner** přidejte modul **Blok textu** pod modul **Registrace partnera**. Zde můžete definovat některé podmínky procesu registrace.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.

### <a name="create-a-business-partner-request-confirmation-page"></a>Vytvořte stránku potvrzení požadavku obchodního partnera

Po odeslání požadavku obchodního partnera by se uživateli měla zobrazit potvrzovací stránka, která potvrdí odeslání. 

Chcete-li nastavit a nakonfigurovat stránku potvrzení požadavku obchodního partnera v nástroji pro tvorbu webů, postupujte takto.

1. Použijte šablonu **Registrace**, kterou jste vytvořil dříve, k vytvoření stránky s názvem **Potvrzení žádosti partnera**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Do slotu **Kontejner** přidejte modul **Blok obsahu**. V podokně vlastností modulu v části **Nadpis** zadejte **Žádost odeslána**. Do pole **Formátovaný text** zadejte **Vaše žádost byla odeslána**. V části **Odkazy** nakonfigurujte odkaz na domovskou stránku a zadejte **Zpět k nákupu** jako text odkazu.
1. Přidejte další modul **Kontejner** a přidejte k němu modul **Kolekce produktů**.
1. Nakonfigurujte modul **Kolekce produktů** se seznamem doporučení nebo kategorií, které chcete na stránce předvést.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.

Chcete-li přidat odkaz na stránku potvrzení požadavku obchodního partnera v nástroji pro tvorbu webů, postupujte takto.

1. Přejděte na stránku **Žádost obchodního partnera**, kterou jste vytvořili dříve, a vyberte **Upravit**. 
1. Vyberte slot modulu **Registrace partnera**. V podokně vlastností v části **Odkaz na stránku Potvrzení registrace** nakonfigurujte odkaz na stránku požadavku obchodního partnera, kterou jste vytvořili dříve. 
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Přidejte odkaz na požadavek obchodního partnera na domovskou stránku

Poté, co se vytvoří stránka pro registraci a potvrzení požadavku obchodního partnera, musíte stránku pro přihlášení zpřístupnit prostřednictvím odkazu na domovské stránce. Tuto úlohu můžete dokončit přidáním odkazu na libovolný modul **Blok obsahu** na domovské stránce.

Chcete-li přidat odkaz na požadavek obchodního partnera na domovskou stránku v nástroji pro tvorbu webů, postupujte takto.

1. Jděte na domovskou stránku vašeho webu a vyberte **Upravit**.
1. Vyberte slot modulu **Blok obsahu**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na stránku požadavku obchodního partnera, kterou jste vytvořili dříve, a zadejte **Zaregistrujte se jako obchodní partner** nebo podobný text jako text odkazu. Podle potřeby přidejte obrázek.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="account-management-landing-page"></a>Cílová stránka správy obchodního vztahu

Vstupní stránka pro správu účtu obsahuje všechny informace o správě účtu, které jsou vyžadovány pro weby elektronického obchodování B2B i B2C. Tuto stránku mohou zobrazit pouze přihlášení uživatelé.

Chcete-li vytvořit a nakonfigurovat cílovou stránku pro správu účtů B2B v nástroji pro tvorbu webů, postupujte takto.

1. Vytvořte šablonu s názvem **Správa účtu**. Tato šablona by měla obsahovat následující moduly:

    - Záhlaví
    - Zápatí
    - Popis cesty
    - Uvítací dlaždice účtu
    - Obecná dlaždice účtu
    - Dlaždice Adresa účtu
    - Dlaždice seznamu požadovaných položek účtu
    - Dlaždice adresy účtu
    - Dlaždice věrnostního programu účtu
    - Dlaždice Zůstatek účtu zákazníka
    - Dlaždice šablon objednávek účtu
    - Uživatelé organizace
    - Seznam obchodních organizací
    - Zůstatek účtu zákazníka
    - Řádky šablony objednávky
    - Seznam šablon objednávek
    - Dlaždice Faktura účtu
    - Seznam faktur
    - Podrobnosti faktury

1. Použijte šablonu **Správa účtu** k vytvoření stránky s názvem **Můj účet**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**. 
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na domovskou stránku a zadejte **Domovská stránka** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **Uvítací dlaždice**. V podokně vlastností modulu v části **Nadpis** zadejte **Vítejte**.
1. Do slotu **Hlavní** přidejte modul **Kontejner** (**Kontejner 2**). V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**. Nastavte hodnotu **Zobrazené podřízené položky** na **Dvě**. 
1. Do slotu **Kontejner 2** přidejte modul **Obecná dlaždice účtu**. V podokně vlastností modulu v části **Nadpis** zadejte **Můj profil**. V položce **Odkazy** nakonfigurujte odkaz na stránce **Můj profil**. 
1. Do slotu **Kontejner 2** přidejte další modul **Obecná dlaždice účtu**. V podokně vlastností modulu v části **Nadpis** zadejte **Historie objednávek**. V položce **Odkazy** nakonfigurujte odkaz na stránku historie objednávek.
1. Do slotu **Hlavní** přidejte modul **Kontejner** (**Kontejner 3**). V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**. Nastavte hodnotu **Zobrazené podřízené položky** na **Dvě**. 
1. Do slotu **Kontejner 3** přidejte modul **Dlaždice adresy účtu**. V podokně vlastností modulu v části **Nadpis** zadejte **Moje adresa**. V položce **Odkazy** nakonfigurujte odkaz na stránce **Moje adresa**. 
1. Do slotu **Kontejner 3** přidejte modul **Dlaždice seznamu přání účtu**. V podokně vlastností modulu v části **Nadpis** zadejte **Můj seznam přání**. V položce **Odkazy** nakonfigurujte odkaz na stránce **Můj seznam přání**.
1. Do slotu **Hlavní** přidejte modul **Kontejner** (**Kontejner 4**). V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**. Nastavte hodnotu **Zobrazené podřízené položky** na **Dvě**. 
1. Do slotu **Kontejner 4** přidejte modul **Uživatelé organizace**. V podokně vlastností modulu v části **Nadpis** zadejte **Uživatelé organizace**. 
1. Do slotu **Kontejner 4** přidejte modul **Dlaždice zůstatku účtu zákazníka**. V podokně vlastností modulu v části **Nadpis** zadejte **Kredit na účtu**. 
1. Do slotu **Hlavní** přidejte modul **Kontejner** (**Kontejner 5**). V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**. Nastavte hodnotu **Zobrazené podřízené položky** na **Dvě**. 
1. Do modulu **Kontejner 5** přidejte modul **Dlaždice šablon objednávek na účtu**. V podokně vlastností modulu v části **Nadpis** zadejte **Šablony objednávek**. 
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

> [!NOTE] 
> Některé z oddílů, které jste přidali v krocích 13 až 18, se neobjeví na plátně WYSIWIG v nástroji pro tvorbu webů, protože vyžadují přihlášený účet B2B.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Vytvářejte a konfigurujte stránky a moduly zůstatku zákazníků 

K úhradě objednávek lze použít zákaznické účty. Disponibilní zůstatek na účtu zákazníka lze zobrazit na stránce správy účtu uživatele.

### <a name="create-a-customer-balance-page"></a>Vytvořte stránku zůstatku zákazníka 

Než si přihlášení uživatelé B2B mohou prohlédnout své zákaznické zůstatky, musíte vytvořit stránku se zůstatky zákazníků. 

Chcete-li vytvořit stránku se zůstatky zákazníků v nástroji pro tvorbu webu, postupujte následovně.

1. Použijte šablonu **Správa účtu**, kterou jste vytvořili dříve k vytvoření stránky s názvem **Zůstatek zákazníka**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner** (**Kontejner 3**). V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**. Nastavte hodnotu **Zobrazené podřízené položky** na **Dvě**.
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na cílovou stránku správy účtu a zadejte **Můj účet** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **Zůstatek na účtu zákazníka**. V podokně vlastností modulu v části **Nadpis** zadejte **Zůstatek na účtu**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.
1. Přejděte na cílovou stránku správy účtu (**Můj účet**), kterou jste vytvořili dříve.
1. V podokně vlastností pro modul **Dlaždice zůstatku na účtu zákazníka** přidejte odkaz na stránku zůstatku zákazníka. 
1. Uložte a publikujte stránku.

Stránka se zůstatkem zákazníků byla nyní vytvořena a uživatelé k ní mají přístup ze vstupní stránky pro správu účtu.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Nakonfigurujte stránku pokladny, aby bylo možné zůstatek zákazníka použít jako způsob platby

Modul **Platba z účtu zákazníka** je nutný k tomu, aby bylo možné zůstatek zákazníka použít jako způsob platby. Tento modul by měl být přidán na stránku pokladny jako způsob platby. Informace o tom, jak nakonfigurovat stránku pokladny a moduly, které jsou nutné k pokladně, včetně všech platebních údajů, viz [Modul pokladny](../add-checkout-module.md).

Po nakonfigurování stránky pokladny musíte přidat modul **Platba z účtu zákazníka** do sekce plateb a poté stránku uložte a publikujte. Uživatelé B2B se poté budou moci přihlásit na web elektronického obchodování a použít svůj zůstatek na zákaznickém zůstatku během objednávek.

Kromě toho se v **Nástroj pro tvorbu webu \> Rozšíření** musíte se ujistit, že je vlastnost **Povolit platby ze zákaznického účtu** nastavena na **Povoleno pro zákazníky B2B**.

## <a name="create-order-template-pages"></a>Vytvořte stránky šablon objednávek

Pro web elektronického obchodu B2B lze nastavit dvě stránky šablon objednávek: stránku se seznamem šablon objednávek a stránku s řádky šablon objednávek.

Stránka se seznamem šablon objednávek zobrazuje seznam všech šablon objednávek, které jsou k dispozici. Nastavuje se pomocí modulu **Seznam šablon objednávek**. Stránka se seznamem šablon objednávek vám umožňuje vytvořit nebo odstranit šablonu a přidat položky v šabloně do košíku.

Stránka řádků šablony objednávky zobrazuje podrobnosti o šabloně objednávky, která je vybrána na stránce se seznamem šablon objednávek. Nastavuje se pomocí modulu **Řádky šablon objednávek**. Když uživatel vybere název šablony na stránce se seznamem šablon objednávek, zobrazí se stránka s řádky šablon objednávek a zobrazí podrobnosti o šabloně. Uživatel pak může zobrazit a upravit položky v šabloně.

### <a name="create-an-order-templates-list-page"></a>Vytvořte stránku se seznamem šablon objednávek

Chcete-li vytvořit stránku se seznamem šablon objednávek v nástroji pro tvorbu webu, postupujte následovně.

1. Použijte šablonu **Správa účtu**, kterou jste vytvořili dříve k vytvoření stránky s názvem **Šablony objednávek**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na cílovou stránku správy účtu a zadejte **Můj účet** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **Seznam šablon objednávek**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.
1. Přejděte na cílovou stránku správy účtu (**Můj účet**), kterou jste vytvořili dříve.
1. V podokně vlastností pro modul **Dlaždice šablon objednávek účtu** v části **Odkazy** nakonfigurujte odkaz na stránku seznamu šablon objednávek, kterou jste právě vytvořili.
1. Uložte a publikujte stránku.

Stránka se seznamem šablon objednávek byla nyní vytvořena a uživatelé k ní mají přístup ze vstupní stránky pro správu účtu.

### <a name="create-an-order-template-lines-page"></a>Vytvořte stránku s řádky šablon objednávek

Chcete-li vytvořit stránku s řádky šablon objednávek v nástroji pro tvorbu webu, postupujte následovně.

1. Použijte šablonu **Správa účtu**, kterou jste vytvořili dříve k vytvoření stránky s názvem **Řádky šablon objednávek**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na cílovou stránku správy účtu a zadejte **Můj účet** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **Řádky šablon objednávek**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.

## <a name="onboard-business-partner-users"></a>Nábor uživatelů obchodních partnerů

Stránka Uživatelé v organizaci umožňuje správci organizace obchodního partnera připojit další uživatele z této organizace na web elektronického obchodování B2B. Nastavuje se pomocí modulu **Seznam obchodních organizací**. Na stránce uživatelů v organizaci může správce přidávat nebo odebírat uživatele, definovat zůstatky na účtech a vyžadovat výkazy uživatele.

Chcete-li vytvořit stránku s uživateli organizace v nástroji pro tvorbu webu, postupujte následovně.

1. Použijte šablonu **Správa účtu**, kterou jste vytvořili dříve k vytvoření stránky s názvem **Uživatelé organizace**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na cílovou stránku správy účtu a zadejte **Můj účet** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **Seznam obchodních organizací**. V podokně vlastností modulu v části **Nadpis** zadejte **Uživatelé organizace**.
1. V podokně vlastností modulu **Seznam obchodních organizací** povolte vlastnosti **Třídění tabulky** a **Stránkování tabulky**. Nastavte počet stránkování na **5**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.
1. Přejděte na cílovou stránku správy účtu (**Můj účet**), kterou jste vytvořili dříve.
1. V podokně vlastností pro modul **Dlaždice uživatelů organizace** v části **Odkazy** nakonfigurujte odkaz na stránku uživatelů organizace, kterou jste právě vytvořili. 
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="create-invoice-pages"></a>Vytvoření stránek faktur

Stránka se seznamem faktur zobrazuje seznam všech dostupných faktur. Nastavuje se pomocí modulu **InvoiceList**. Na stránce se seznamem faktur mohou uživatelé hradit nebo požadovat faktury. 

Stránka s podrobnostmi o faktuře zobrazuje podrobnosti o faktuře, která je vybrána na stránce se seznamem faktur. Nastavuje se pomocí modulu **Podrobnosti faktur**. Když uživatel vybere ID faktury na stránce se seznamem faktur, zobrazí se stránka s podrobnostmi o faktuře a zobrazí podrobnosti faktury.

### <a name="create-an-invoices-list-page"></a>Vytvořte stránku se seznamem faktur

Chcete-li vytvořit stránku se seznamem faktur v nástroji pro tvorbu webu, postupujte následovně.

1. Použijte šablonu **Správa účtu**, kterou jste vytvořili dříve k vytvoření stránky s názvem **Seznam faktur**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na cílovou stránku správy účtu a zadejte **Můj účet** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **InvoicesList**. V podokně vlastností modulu v části **Nadpis** zadejte **Faktury**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.
1. Přejděte na cílovou stránku správy účtu (**Můj účet**), kterou jste vytvořili dříve.
1. V podokně vlastností pro modul **Dlaždice faktur účtu** v části **Odkazy** nakonfigurujte odkaz na stránku seznamu faktur, kterou jste právě vytvořili. 
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="create-an-invoice-details-page"></a>Vytvořte stránku s podrobnostmi o faktuře

Chcete-li vytvořit stránku s podrobnostmi o fakturách v nástroji pro tvorbu webu, postupujte následovně.

1. Použijte šablonu **Správa účtu**, kterou jste vytvořili dříve k vytvoření stránky s názvem **Podrobnosti faktur**.
1. Do slotu **Záhlaví** přidejte fragment záhlaví, který je předkonfigurovaný se záhlavím webu.
1. Do slotu **Zápatí** přidejte fragment zápatí, který je předkonfigurovaný se zápatím webu.
1. Do slotu **Hlavní** přidejte modul **Kontejner**. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Do slotu **Kontener** přidejte modul **Popis cesty**. V podokně vlastností modulu v části **Odkazy** nakonfigurujte odkaz na cílovou stránku správy účtu a zadejte **Můj účet** jako text odkazu. Poté nakonfigurujte odkaz na stránku se seznamem faktur a zadejte **Seznamy faktur** jako text odkazu.
1. Do slotu **Kontejner** přidejte modul **Podrobnosti faktur**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Publikujte adresu URL stránky.

## <a name="add-a-quick-add-module-to-the-cart-page"></a>Přidání modulu rychlého přidání na stránku košíku

Modul rychlého přidání poskytuje způsob, jak rychle přidat více položek do košíku pomocí ID položek (známé také jako ID skladových jednotek \[SKU\]). Modul rychlého přidání je přidán na stránku košíku webu.

Chcete-li přidat modul rychlého přidání na stránku košíku v konfigurátoru webů Commerce, postupujte následujícím způsobem.

1. Přejděte k možnosti **Šablony** a vyberte šablonu stránky košíku na vašem webu.
1. Vyberte možnost **Upravit**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Přidat rychlý odkaz** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte k možnosti **Stránky** a vyberte šablonu stránky košíku na vašem webu.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu **Kontejner** nastavte vlastnost **Šířka** na hodnotu **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Přidat rychlý odkaz** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

> [!NOTE] 
> Modul rychlého přidání je k dispozici od verze Commerce 10.0.17. Pokud provádíte aktualizaci ze starší verze Commerce, musíte ručně aktualizovat soubor appsettings.json. Další pokyny viz [SDK a aktualizace knihovny modulů](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="add-a-bulk-purchase-module-to-a-product-details-page"></a>Přidání modulu hromadného nákupu na stránku podrobností o produktu

Modul hromadného nákupu na stránce s podrobnostmi o produktu poskytuje maticové prostředí, které kupujícímu umožňuje rychle přidat do košíku více variant produktu. Když uživatel webu musí objednat více variant stejného produktu, toto prostředí eliminuje potřebu vybrat kombinaci rozměrů produktu, definovat množství, přidat variantu do košíku a poté opakovat proces pro další kombinace rozměrů produktu.

Modul hromadného nákupu přidáte na stránku s podrobnostmi o produktu v konfigurátoru webů Commerce tímto postupem.

1. Přejděte k možnosti **Šablony** a vyberte šablonu stránky s podrobnostmi o produktu na vašem webu.
1. Vyberte možnost **Upravit**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Hromadný nákup** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte k možnosti **Stránky** a vyberte stránku s podrobnostmi o produktu na vašem webu.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu **Kontejner** nastavte vlastnost **Šířka** na hodnotu **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Hromadný nákup** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

> [!NOTE] 
> Modul hromadného nákupu je k dispozici od verze Commerce verze 10.0.24. Pokud provádíte aktualizaci ze starší verze Commerce, musíte ručně aktualizovat soubor appsettings.json. Další pokyny viz [SDK a aktualizace knihovny modulů](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](../starter-kit-overview.md)

[SDK a aktualizace knihovny modulů](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

[Přehled stránky pro tvorbu](../authoring-home-overview.md)

[Přehled šablon a rozvržení](../templates-layouts-overview.md)

[Práce s fragmenty](../work-with-fragments.md)

[Přidání nové webové stránky](../add-new-page.md)

[Modul pokladny](../add-checkout-module.md)

[Modul bloku obsahu](../add-hero-module.md)

[Modul kolekce produktů](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
