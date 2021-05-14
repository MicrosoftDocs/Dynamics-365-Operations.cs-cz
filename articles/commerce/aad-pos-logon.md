---
title: Konfigurace ověření Azure Active Directory pro přihlášení do POS
description: Toto téma vysvětluje, jak konfigurovat Azure Active Directory jako metodu ověřování v místě prodeje Microsoft Dynamics 365 Commerce.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937451"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Konfigurace ověření Azure Active Directory pro přihlášení do POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma vysvětluje, jak konfigurovat Azure Active Directory (Azure AD) jako metodu ověřování v místě prodeje (POS) Microsoft Dynamics 365 Commerce.

Maloobchodníci, kteří používají Dynamics 365 Commerce spolu s dalšími cloudovými službami společnosti Microsoft, jako je Microsoft Azure, Microsoft 365 a Microsoft Teams, obvykle chtějí použít Azure AD pro centralizovanou správu pověření uživatele pro bezpečné a bezproblémové přihlašování mezi aplikacemi. Chcete-li použít ověřování Azure AD pro Commerce POS, musíte nejprve nakonfigurovat Azure AD jako metodu ověřování v centrále Commerce.

## <a name="configure-pos-authentication-method"></a>Konfigurace metody ověřování POS

Konfiguraci metody ověřování POS v centrále Commerce provedete následovně.
    
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily** a zvolte profil funkcí, který chcete změnit.
1. V části **Přihlášení zaměstnanců POS** rychlé karty **Funkce** vyberte požadovanou možnost metody ověřování z rozbalovacího seznamu **Metoda ověřování přihlášení**.

    **Metoda ověřování přihlášení** má tři možnosti:
    
    - **ID pracovníka a heslo** – Tato výchozí možnost vyžaduje, aby uživatelé POS zadali osobní ID a heslo pro přihlášení k POS a pro přístup k funkcím přepsání správce.
    - **Azure AD bez jednotného přihlášení** – Tato možnost vyžaduje, aby uživatelé POS používali přihlašovací údaje Azure AD pro přihlášení do POS a přístupu k funkci přepsání správce. Když je POS klient obnoven nebo znovu otevřen, musí uživatel POS znovu zadat přihlašovací údaje Azure AD pro opětovné přihlášení.
    - **Azure AD s jednotným přihlášením** – Když je vybrána tato možnost, uživatelé POS se mohou přihlásit do cloudového POS (CPOS) pomocí aktivních přihlašovacích údajů Azure AD, které používají jiné webové aplikace ve stejném webovém prohlížeči, nebo se přihlásí pomocí Modern POS (MPOS) pomocí přihlašovacích údajů Azure AD přihlášených k systému Windows. Obě metody umožňují přihlášení bez nutnosti zadávat přihlašovací údaje Azure AD na přihlašovací obrazovce POS. Přístup k funkci přepsání správce POS však bude i nadále vyžadovat přihlášení pomocí přihlašovacích údajů Azure AD.

1. Přejděte na **Retail a Commerce > IT Retail a Commerce IT > Distribuční plán** a spusťte úlohu **1070 (konfigurace kanálu)** k synchronizaci nejnovějšího nastavení profilu funkce s klienty POS.

> [!NOTE]
> - Možnost metody ověřování **Azure AD bez jednotného přihlášení** nahrazuje možnost **Azure Active Directory** v Commerce verzi 10.0.18 a starší.
> - ověřování Azure AD vyžaduje aktivní připojení k internetu a nebude fungovat, když je POS offline.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Přidružení účtů Azure AD s uživateli POS

Chcete-li použít Azure AD jako metodu ověřování POS, musíte přidružit účty Azure AD s uživateli POS v centrále Commerce. 

Chcete-li přidružit účty Azure AD s uživateli POS v ústředí Commerce, postupujte takto.
    
1. Přejděte na **Retail a Commerce > Zaměstnanci> Pracovníci** a otevřete záznam pracovníka.
1. V podokně akcí vyberte kartu **Commerce** poté ve skupině **Externí identita** zvolte **Přidružit existující identitu**. 
1. V dialogovém okně **Použít existující externí identitu** vyberte možnost **Hledat pomocí e-mailu**, zadejte e-mailovou adresu Azure AD a pak vyberte možnost **Hledat**.
1. Vyberte požadovaný účet Azure AD a poté vyberte tlačítko **OK**.

Po provedení výše uvedeného postupu konfigurace Pole **Alias**, **UPN** a **Externí dílčí identifikátor** na kartě **Commerce** na stránce Podrobnosti pracovníka budou vyplněna.

Musíte spustit úlohu **1060 (zaměstnanci)** v **Retail a Commerce > IT Retail a Commerce > Distribuční plán** k synchronizaci nejnovějšího uživatele POS a dat účtu Azure AD do kanálu.

> [!NOTE]
> Jako osvědčený postup je po aktualizací údajů o pracovníkovi, jako je heslo, oprávnění POS, přidružený účet Azure AD nebo adresář zaměstnance, v centrále Commerce, je velmi doporučeno spustit úlohu **1060 (zaměstnanci)** pro synchronizaci nejnovějších informací o pracovníkovi s kanálem. Klient POS pak může načíst správná data pro ověření uživatele a kontrolu autorizace.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Odhlášení od pokladny POS a odhlášení pomocí ověřování Azure AD

Když je POS nakonfigurován pro použití metody ověřování Azure AD, dojde k následujícímu:

- Funkce **Uzamknout pokladnu** nebude v aplikaci POS k dispozici. 
- Funkce **Automaticky uzamknout** se bude chovat stejně jako funkce **Automatické odhlášení**.
- Pokud uživatel POS zvolí **Odhlásit se**, bude uživatel vyzván k přihlášení pomocí přihlašovacích údajů Azure AD při příštím spuštění POS, bez ohledu na to, zda je povoleno jednotné přihlášení.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Funkce přepsání správce pomocí ověřování Azure AD

Když je POS nakonfigurován k použití ověřování Azure AD, funkce přepsání správce otevře dialogové okno s výzvou pro zadání přihlašovacích údajů uživatele správce Azure AD. Po schválení přihlášení správce budou přihlašovací údaje Azure AD správce zrušena a přihlašovací údaje předchozího uživatele Azure AD budou použita pro následné operace POS.

> [!NOTE]
> - V Commerce verzí 10.0.18 a starších nepodporuje funkce přepsání správce Azure AD. ID pracovníka a heslo jsou povinné, i když je POS nakonfigurována na použití metody ověřování Azure AD.
> - Pokud používáte CPOS s webovým prohlížečem Safari na zařízení Apple iOS, musíte nejprve vypnout **Blokovat vyskakovací okna** v nastavení Safari, aby přepsání funkcí správce fungovalo s ověřováním Azure AD. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Osvědčené postupy zabezpečení pro ověřování POS na základě Azure AD na sdílených zařízeních

Mnoho maloobchodníků nastavuje prostředí maloobchodních prodejen tak, aby více uživatelů potřebovalo přístup k aplikaci POS ze sdíleného fyzického zařízení. V tomto kontextu, zatímco jednotné přihlášení poskytuje pohodlné a bezproblémové ověřování, může také vytvořit bezpečnostní mezeru, kde si aktuální uživatel POS nemusí uvědomit, že při provádění transakcí nebo operací v POS se používají přihlašovací údaje jiného uživatele. Před konfigurací POS pro použití metody ověřování Azure AD důrazně doporučujeme zkontrolovat zásady zabezpečení a nastavení přihlášení sdíleného zařízení a rozhodnout, která možnost je nejvhodnější.

- Pokud vaše maloobchodní prostředí používá pro přihlášení fyzického zařízení sdílený účet (například místní účet), doporučuje se použít možnost **Azure AD bez jednotného přihlášení**. Tím je zajištěno, že každý uživatel POS výslovně zadává přihlašovací údaje Azure AD pro přihlášení k POS.
- Pokud vaše prostředí maloobchodu vyžaduje, aby zaměstnanci používali své vlastní účty Azure AD pro přihlášení k POS a hostuje fyzické zařízení, doporučuje se použít možnost **Azure AD s jednotným přihlášením**.

## <a name="additional-resources"></a>Další prostředky

[ Konfigurace pracovníka](tasks/worker.md)

[Vytvoření funkčního profilu maloobchodu](retail-functionality-profile.md)


[Nastavení funkce rozšířeného přihlášení pro MPOS a Cloud POS](extended-logon.md)

[Osvědčené postupy zabezpečení pro Cloud POS ve sdílených prostředích](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
