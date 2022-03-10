---
title: Profily certifikátů definované uživatelem pro maloobchodní prodejny
description: Toto téma poskytuje přehled o tom, jak se certifikáty používají v maloobchodních prodejnách.
author: josaw
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cb82a6d6336bb69fe818fb33e04ad621382b383055b24a4e79eee5ddff217ac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719923"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Profily certifikátů definované uživatelem pro maloobchodní prodejny

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Přehled

Toto téma obsahuje přehled certifikátových profilů dostupných v Microsoft Dynamics 365 Commerce. Tato funkce rozšiřuje funkci [Správa tajných kódů pro kanály Retail](../dev-itpro/manage-secrets.md) přidáním podpory pro místní certifikáty.

Když pokladní místo běží v offline režimu, nemůže pracovat s certifikáty, které jsou uloženy v trezoru klíčů. Místo toho by měl být použit místní certifikát. Podporovány jsou následující schopnosti:

- Použití místních certifikátů v záložních scénářích trezoru klíčů
- Použití místních certifikátů bez trezoru klíčů (například v místní instalaci)
- Postupná aktualizace certifikátů, kdy některé obchody a terminály používají novou verzi certifikátu, ale jiné obchody a terminály nadále používají předchozí verzi

Funkce profilů certifikátů umožňuje určit výchozí certifikát a nastavit pořadí, ve kterém budou certifikáty ve stejném profilu certifikátu prohledávány. Tato funkce také poskytuje podobný přístup k nastavení pro místní certifikáty a certifikáty Key Vault. Pro certifikáty můžete přidat nastavení specifické pro společnost, ale v kanálech Commerce lze použít jedinečný identifikátor pro každou společnost.

### <a name="scenarios"></a>Scénáře

Funkce profilů certifikátů podporuje následující scénáře v kanálech Commerce:

- Používáte místní certifikát v záložních scénářích trezoru klíčů. Následuje několik příkladů těchto záložních scénářů:

    - Úložiště trezoru klíčů není přístupné.
    - V úložišti trezoru klíčů nebyl nalezen certifikát.
    - Pokladní místo běží v offline režimu.

- Používáte místní certifikáty, ale bez jejich uložení v trezoru klíčů (například v místní instalaci).
- Provádíte postupnou aktualizaci certifikátů, kdy se nová verze certifikátu používá pouze v obchodech nebo na terminálech, kde je nová verze již k dispozici.
- Používáte stejný certifikát v několika společnostech.

## <a name="set-up-certificate-profiles"></a>Nastavení profilů certifikátů

Následující postup vysvětluje, jak nastavit profily certifikátů. Před použitím profilů certifikátů v kanálech Commerce nakonfigurujte nastavení podle těchto pokynů.

1. V pracovním prostoru **Správa funkcí** zapněte funkci **Profily certifikátů definované uživatelem pro maloobchodní prodejny**.
2. Přejděte do nabídky **Správa systému \> Nastavení \> Profily certifikátů**.
3. Vytvořte záznam a nastavte pro něj pole **Profil certifikátu**, **Název** a **Popis**.

    > [!NOTE]
    > Profil certifikátu je jedinečný identifikátor certifikátu ve všech společnostech a komponentách Commerce.

3. Na kartě **Právnické osoby** přidejte řádek a vyberte právnickou osobu (společnost), pro kterou by se měl aktuální profil certifikátu používat. Pokud by se měl profil certifikátu používat pro více právnických osob, opakujte tento krok a přidejte řádek pro každou další právnickou osobu.
4. Vyberte **Nastavení** a otevře se stránka **Nastavení profilu certifikátu**, kde můžete pro profil certifikátu zadat nastavení specifické pro společnost.

### <a name="certificate-profile-settings"></a>Nastavení profilů certifikátů

Když vyberete **Nastavení** pro řádky profilu certifikátu, zobrazí se stránka **Nastavení profilu certifikátu**. Na této stránce můžete určit, které certifikáty lze použít, když se v kanálech Commerce volá aktuální profil certifikátu. Můžete také určit pořadí, ve kterém mají být certifikáty prohledávány.

> [!NOTE]
> Pole **Priorita** se nastaví automaticky. Hodnota **1** představuje nejvyšší prioritu. Když je na stránku **Nastavení profilu certifikátu** přidán nový řádek, jeho priorita je nastavena na číslo, které je o jednu větší než priorita předchozího řádku. Chcete-li změnit prioritu konkrétního řádku, vyberte ho a poté vyberte buď možnost **Posunout nahoru**, která prioritu zvýší, nebo možnost **Posunout dolů**, která priorita sníží.

Když přidáte nový řádek na stránku **Nastavení profilu certifikátu**, nastavte následující pole:

- **Typ umístění** – Vyberte umístění, kde je certifikát uložen. Toto pole má dvě možné hodnoty: **Místní certifikát** a **Key Vault**.
- **Certifikát Key Vault** – Toto pole je povinné, pokud nastavíte pole **Typ umístění** na **Key Vault**. Slouží k určení tajného kódu certifikátu Key Vault.

    > [!NOTE]
    > Před použitím certifikátu Key Vault v profilech certifikátů nahrajte certifikát do úložiště trezoru klíčů a postupujte podle pokynů v článku [Nastavení klienta Azure Key Vault](../../finance/localizations/setting-up-azure-key-vault-client.md).

- **Název obchodu** – Toto pole je volitelné a je k dispozici, pouze pokud nastavíte pole **Typ umístění** na **Místní certifikát**. Slouží k určení výchozího názvu obchodu, který by se měl použít k hledání v místních certifikátech.
- **Umístění obchodu** – Toto pole je volitelné a je k dispozici, pouze pokud nastavíte pole **Typ umístění** na **Místní certifikát**. Slouží k určení výchozího místa obchodu, který by se měl použít k hledání v místních certifikátech.

    > [!NOTE]
    > Výchozí název obchodu a umístění obchodu se přidávají proto, aby se zjednodušil proces hledání místních certifikátů v modulu Commerce Runtime. X509StoreProvider má seznam složek, kde jsou certifikáty uloženy. Pokud není zadán výchozí název obchodu a výchozí umístění obchodu, pokusí se X509StoreProvider najít certifikát v ostatních složkách ve svém seznamu.

- **Kryptografický otisk** – Toto pole je povinné a je k dispozici, pouze pokud nastavíte pole **Typ umístění** na **Místní certifikát**. Slouží k zadání kryptografického otisku certifikátu.
- **Komentáře** – Toto pole je volitelné a umožňuje uživatelům zadávat poznámky.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Pracovní postup: Hledání certifikátů v modulu Commerce Runtime

Tady je základní pracovní postup, který se používá k vyhledání certifikátu, když je v modulu Commerce Runtime volán profil certifikátu.

1. Systém identifikuje, zda má profil certifikátu specifické nastavení společnosti pro aktuální právnickou osobu.
1. Systém se pokusí najít certifikát pomocí hodnot na stránce **Nastavení profilu certifikátu** pro řádek, kde je pole **Priorita** nastaveno na **1**.

    - Pokud je pole **Typ umístění** nastaveno na **Key Vault**, použije se k vyhledání certifikátu na stránce **Parametry trezoru klíčů** hodnota pole **Tajný kód certifikátu Key Vault**. Certifikát se poté vyhledá v úložišti trezoru klíčů.
    - Pokud je pole **Typ umístění** nastaveno na **Místní certifikát**, X509StoreProvider nejprve vyhledá certifikát pomocí výchozího názvu obchodu a umístění obchodu, pokud jsou tyto parametry zadány. Poté prohledá všechny ostatní složky ve svém seznamu složek.

1. Pokud certifikát nebyl nalezen, proces se opakuje pro řádek, kde je pole **Priorita** nastaveno na **2** a tak dále.

> [!NOTE]
> Pokud profil certifikátu nemá žádná nastavení pro aktuální právnickou osobu, nebo pokud je vyhledávání certifikátu neúspěšné pro všechny řádky na stránce **Nastavení profilu certifikátu**, certifikát nebyl nalezen.

#### <a name="caching-the-results-of-certificate-searches"></a>Ukládání výsledků vyhledávání certifikátů do mezipaměti

Výsledky vyhledávání certifikátů se ukládají do mezipaměti. Výchozí doba platnosti mezipaměti je jedna hodina. Tuto dobu však lze přizpůsobit a lze ji nastavit na maximální hodnotu 24 hodin.

### <a name="gradual-update"></a>Postupná aktualizace

Pokud je zavedena nová verze certifikátu, ale nelze ho aktualizovat ve všech obchodech současně, funkce profilů certifikátů umožní postupnou aktualizaci certifikátu.

1. Najděte profil certifikátu a řádek, který by měl být aktualizován, a poté vyberte **Nastavení**.
1. Přidejte řádek a určete nastavení, která souvisí s nejnovější verzí certifikátu.
1. Zvyšte hodnotu **Priorita** nového řádku. Pomocí tlačítka **Posunout nahoru** přesuňte řádek tak, aby byl nad řádkem pro předchozí verzi stejného certifikátu.

> [!NOTE]
> V modulu Commerce Runtime bude nejprve volána nová verze certifikátu. Pokud certifikát ještě nebyl aktualizován v konkrétním obchodě nebo na konkrétním terminálu, bude volána předchozí verze.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]