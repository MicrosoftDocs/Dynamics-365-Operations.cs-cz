---
title: Profily certifikátů definovaných uživatelem pro maloobchodní prodejny
description: Tento článek obsahuje přehled certifikátových profilů dostupných v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558430"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Profily certifikátů definovaných uživatelem pro maloobchodní prodejny

[!include [banner](../includes/banner.md)]

Tento článek obsahuje přehled certifikátových profilů dostupných v Microsoft Dynamics 365 Commerce. Tato funkce rozšiřuje funkci [Správa tajných kódů pro kanály Retail](../dev-itpro/manage-secrets.md) přidáním podpory pro místní certifikáty.

Když pokladní místo běží v offline režimu, nemůže pracovat s certifikáty, které jsou uloženy v řešení Microsoft Azure Key Vault. Místo toho by měl být použit místní certifikát. Podporovány jsou následující schopnosti:

- Použití místních certifikátů v záložních scénářích úložiště Key Vault
- Použití místních certifikátů bez úložiště Key Vault (například v místní instalaci)
- Postupná aktualizace certifikátů, kdy některé obchody a terminály používají novou verzi certifikátu, ale jiné obchody a terminály nadále používají předchozí verzi

Funkce profilů certifikátů umožňuje určit výchozí certifikát a nastavit pořadí, ve kterém budou certifikáty ve stejném profilu certifikátu prohledávány. Tato funkce také poskytuje podobný přístup k nastavení pro místní certifikáty a certifikáty Key Vault. Pro certifikáty můžete přidat nastavení specifické pro společnost, ale v kanálech Commerce lze použít jedinečný identifikátor pro každou společnost.

### <a name="scenarios"></a>Scénáře

Funkce profilů certifikátů podporuje následující scénáře v kanálech Commerce:

- Používáte místní certifikát v záložních scénářích úložiště Key Vault. Následuje několik příkladů těchto záložních scénářů:

    - Úložiště trezoru klíčů není přístupné.
    - V úložišti trezoru klíčů nebyl nalezen certifikát.
    - Pokladní místo běží v offline režimu.

- Používáte místní certifikáty, ale bez jejich uložení v úložišti Key Vault (například v místní instalaci).
- Provádíte postupnou aktualizaci certifikátů, kdy se nová verze certifikátu používá pouze v obchodech nebo na terminálech, kde je nová verze již k dispozici.
- Používáte stejný certifikát v několika společnostech.

## <a name="set-up-certificate-profiles"></a>Nastavení profilů certifikátů

Následující postup vysvětluje, jak nastavit profily certifikátů.

### <a name="set-up-key-vault"></a>Nastavení úložiště Key Vault

Než budete moci používat digitální certifikát, který je uložen v úložišti Key Vault, je třeba provést následující kroky.

1. Vytvořte účet úložiště Key Vault. Účet úložiště doporučujeme nasadit ve stejné geografické oblasti jako Commerce Scale Unit.
1. Do účtu úložiště Key Vault odešlete digitální certifikát.
1. Autorizujte aplikaci Application Object Server (AOS) ke čtení tajných klíčů z účtu úložiště Key Vault.

Další informace, jak pracovat s Key Vault, viz [Začínáme s Azure Key Vault](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Nastavit systémové parametry

Než nakonfigurujete profily certifikátů v kanálech Commerce, musíte povolit službě Commerce používat certifikáty uložené v úložišti Key Vault a profily certifikátů.

Parametry systému v Commerce headquarters nastavíte následovně:

1. Na stránce **Parametry systému** nastavte možnost **Použít pokročilé úložiště certifikátů** jako **Ano**.
1. V pracovním prostoru **Správa funkcí** zapněte funkci **Profily certifikátů definované uživatelem pro maloobchodní prodejny**.

### <a name="set-up-key-vault-parameters"></a>Natavení parametrů úložiště Key Vault

Na stránce **Parametry úložiště Key Vault** musíte zadat následující parametry pro přístup k úložišti Key Vault:

- **Název** a **Popis** – Název a popis účtu úložiště Key Vault.
- **Adresa URL úložiště Key Vault** – Adresa URL účtu úložiště Key Vault.
- **Klient úložiště Key Vault** – ID interaktivního klienta aplikace Azure Active Directory (Azure AD), které je přidruženo k účtu úložiště Key Vault pro účely ověřování. Tento klient by měl mít přístup ke čtení tajných klíčů z účtu úložiště.
- **Tajný klíč úložiště Key Vault** – Tajný klíč, který je přidružen k aplikaci Azure AD, která se používá k ověřování v účtu úložiště Key Vault.
- **Název**, **Popis** a **Odkaz na tajný klíč** – Název, popis a odkaz na tajný klíč certifikátu.

Další informace naleznete v tématu [Nastavení klienta Azure Key Vault](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Konfigurace profilu certifikátu

Konfiguraci profilu certifikátu v Commerce headquarters provedete následovně.

1. Přejděte do nabídky **Správa systému \> Nastavení \> Profily certifikátů**.
1. V podokně akcí vyberte možnost **Nový** a vytvořte záznam.
1. Zadejte hodnoty do polí **Profil certifikátu**, **Název** a **Profil**.

    > [!NOTE]
    > Profil certifikátu je jedinečný identifikátor certifikátu ve všech společnostech a komponentách Commerce.

1. Na záložce s náhledem **Právnické osoby** volbou **Přidat** přidejte řádek.
1. V sekci **Právnická osoba** vyberte právnickou osobu (společnost), pro kterou se má aktuální profil certifikátu používat.

    Pokud by se měl profil certifikátu používat pro více právnických osob, opakujte krok 4 a 5 a přidejte řádek pro každou další právnickou osobu.

1. Vyberte **Nastavení** a otevře se stránka **Nastavení profilu certifikátu**, kde můžete pro profil certifikátu zadat nastavení specifické pro společnost. Zadejte, které certifikáty lze použít, když se v kanálech Commerce volá aktuální profil certifikátu. Přidejte tolik certifikátů, kolik potřebujete, a nastavte pro ně priority. Pokud není k dispozici certifikát s vyšší prioritou, použije se další certifikát na základě priority. Více informací naleznete v části [Pracovní postup: Hledání certifikátů v modulu Commerce Runtime](#workflow-searching-certificates-in-the-commerce-runtime).

    > [!NOTE]
    > Pole **Priorita** se nastaví automaticky. Hodnota **1** představuje nejvyšší prioritu. Když je na stránku **Nastavení profilu certifikátu** přidán nový řádek, jeho priorita je nastavena na číslo, které je o jednu větší než priorita předchozího řádku. Chcete-li změnit prioritu konkrétního řádku, vyberte ho a poté vyberte buď možnost **Posunout nahoru**, která prioritu zvýší, nebo možnost **Posunout dolů**, která priorita sníží.

1. Když přidáte nový řádek na stránku **Nastavení profilu certifikátu**, nastavte následující pole:

    - **Typ umístění** – Vyberte umístění, kde je certifikát uložen. Toto pole má dvě možné hodnoty: **Místní certifikát** a **Key Vault**.
    - **Certifikát Key Vault** – Toto pole je povinné, pokud nastavíte pole **Typ umístění** na **Key Vault**. Slouží k určení tajného kódu certifikátu Key Vault.
    - **Název obchodu** – Toto pole je volitelné a je k dispozici, pouze pokud nastavíte pole **Typ umístění** na **Místní certifikát**. Slouží k určení výchozího názvu obchodu, který by se měl použít k hledání v místních certifikátech.
    - **Umístění obchodu** – Toto pole je volitelné a je k dispozici, pouze pokud nastavíte pole **Typ umístění** na **Místní certifikát**. Slouží k určení výchozího místa obchodu, který by se měl použít k hledání v místních certifikátech.

        > [!NOTE]
        > Výchozí název obchodu a umístění obchodu se přidávají proto, aby se zjednodušil proces hledání místních certifikátů v modulu Commerce Runtime. X509StoreProvider má seznam složek, kde jsou certifikáty uloženy. Pokud není zadán výchozí název obchodu a výchozí umístění obchodu, pokusí se X509StoreProvider najít certifikát v ostatních složkách ve svém seznamu. Další informace o dostupných hodnotách pro název a umístění obchodu naleznete v části [Výčet StoreName](/dotnet/api/system.security.cryptography.x509certificates.storename) a [Výčet StoreLocation](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Kryptografický otisk** – Toto pole je povinné a je k dispozici, pouze pokud nastavíte pole **Typ umístění** na **Místní certifikát**. Slouží k zadání kryptografického otisku certifikátu.

        > [!IMPORTANT]
        > Musíte zajistit, aby uživatel, který spustí aplikaci, která musí používat lokální certifikát (například Modern POS v režimu offline), měl k soukromému klíči certifikátu přístup alespoň pro čtení.

    - **Komentáře** – Toto pole je volitelné a umožňuje uživatelům zadávat poznámky.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Pracovní postup: Hledání certifikátů v modulu Commerce Runtime

Tady je základní pracovní postup, který se používá k vyhledání certifikátu, když je v modulu Commerce Runtime volán profil certifikátu.

1. Systém identifikuje, zda má profil certifikátu specifické nastavení společnosti pro aktuální právnickou osobu.
1. Systém se pokusí najít certifikát pomocí hodnot na stránce **Nastavení profilu certifikátu** pro řádek, kde je pole **Priorita** nastaveno na **1**.

    - Pokud je pole **Typ umístění** nastaveno na **Key Vault**, použije se k vyhledání certifikátu na stránce **Parametry trezoru klíčů** hodnota pole **Tajný kód certifikátu Key Vault**. Certifikát se poté vyhledá v úložišti trezoru klíčů.
    - Pokud je pole **Typ umístění** nastaveno na **Místní certifikát**, X509StoreProvider nejprve vyhledá certifikát pomocí výchozího názvu obchodu a umístění obchodu, pokud jsou tyto parametry zadány. Poté prohledá všechny ostatní složky ve svém seznamu složek.

1. Pokud certifikát nebyl nalezen, proces se opakuje pro řádek, kde je pole **Priorita** nastaveno na **2** a tak dále.

> [!NOTE]
> Pokud profil certifikátu nemá žádná nastavení pro aktuální právnickou osobu, nebo pokud je vyhledávání certifikátu neúspěšné pro všechny řádky na stránce **Nastavení profilu certifikátu**, certifikát nebyl nalezen.

### <a name="caching-the-results-of-certificate-searches"></a>Ukládání výsledků vyhledávání certifikátů do mezipaměti

Výsledky vyhledávání certifikátů se ukládají do mezipaměti. Výchozí doba platnosti mezipaměti je jedna hodina. Tuto dobu však lze přizpůsobit a lze ji nastavit na maximální hodnotu 24 hodin.

## <a name="gradual-update"></a>Postupná aktualizace

Pokud je zavedena nová verze certifikátu, ale nelze ho aktualizovat ve všech obchodech současně, funkce profilů certifikátů umožní postupnou aktualizaci certifikátu.

1. Najděte profil certifikátu a řádek, který by měl být aktualizován, a poté vyberte **Nastavení**.
1. Přidejte řádek a určete nastavení, která souvisí s nejnovější verzí certifikátu.
1. Zvyšte hodnotu **Priorita** nového řádku. Pomocí tlačítka **Posunout nahoru** přesuňte řádek tak, aby byl nad řádkem pro předchozí verzi stejného certifikátu.
> [!NOTE]
> V modulu Commerce Runtime bude nejprve volána nová verze certifikátu. Pokud certifikát ještě nebyl aktualizován v konkrétním obchodě nebo na konkrétním terminálu, bude volána předchozí verze.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
