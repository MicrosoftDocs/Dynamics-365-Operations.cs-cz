---
title: Povolit vyhledávání hlavních dat pro konfiguraci výpočtu daně
description: Tento článek vysvětluje, jak nastavit a aktivovat funkci vyhledávání hlavních dat pro výpočet daně.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181117"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Povolit vyhledávání hlavních dat pro konfiguraci výpočtu daně 

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit a aktivovat funkci vyhledávání hlavních dat pro výpočet daně. K dispozici je rozevírací seznam pro výběr hodnot v konfiguraci výpočtu daně pro pole, například **Právnická osoba**, **Účet dodavatele**, **Kód položky** a **Termín doručení**. Tyto hodnoty pocházejí od připojeného prostředí Microsoft Dynamics 365 Finance s využitím zdroje dat Microsoft Dataverse.

> [!NOTE] 
> Funkce vyhledávání hlavních dat výpočtu daně je volitelná. Pokud deaktivujete funkci **Podpora zdrojů dat Dataverse daňové služby** ve službě Regulatory Configuration Service (RCS), můžete přeskočit následující kroky. V takovém případě však rozevírací seznam nebude dostupný v konfiguraci výpočtu daně.

Chcete-li povolit rozevírací seznam v konfiguraci verze funkce Výpočet daně, proveďte následující kroky.

1. [Aktivujte integraci Microsoft Power Platform a otevřete prostředí Dataverse.](#enable)
2. [Nainstalujte virtuální entity finance a provoz.](#install)
3. [Zaregistrujte aplikaci Azure Active Directory (Azure AD).](#register)
4. [Udělte oprávnění finančním a provozním aplikacím.](#grant)
5. [Nakonfigurujte zdroje dat virtuálních entit.](#configure)
6. [Aktivujte virtuální entity Dataverse.](#virtual)
7. [Nastavte připojenou aplikaci pro výpočet daně.](#set-up)
8. [Importujte a nastavte konfiguraci mapování modelu Dataverse.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Aktivujte integraci Microsoft Power Platform a otevřete prostředí Dataverse

Integraci finančních a provozních aplikací s Microsoft Power Platform lze aktivovat, když vytvoříte nové prostředí finančních a provozních aplikací v Microsoft Dynamics Lifecycle Services (LCS). Další informace naleznete v tématu [Integrace Microsoft Power Platform – Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Po dokončení se název prostředí Microsoft Power Platform objeví v části **Integrace Power Platform**.

1. V LCS, ve vašem finančním a provozním prostředí, v části **Integrace Power Platform** najděte a poznamenejte si hodnotu **Název prostředí** pro propojené prostředí.

    [![Název hodnoty prostředí.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. V [centru pro správu Power Platform](https://admin.powerplatform.microsoft.com/environments) na kartě **Prostředí** vyberte prostředí, které odpovídá hodnotě **Název prostředí**, kterou jste si poznamenali.
3. Na stránce **Podrobnosti** najděte hodnotu **Adresa URL prostředí** prostředí Dataverse. Poznamenejte si tuto hodnotu, protože ji budete potřebovat v [kroku 7. Nastavte připojenou aplikaci pro výpočet daně](#set-up).
4. Ujistěte se, že můžete otevřít prostředí Dataverse ve vašem prohlížeči výběrem hodnoty **Adresa URL prostředí**.

    [![Stránka prostředí Dataverse.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Nechte prostředí Dataverse otevřené ve vašem prohlížeči. Budete ho potřebovat v [kroku 5. Nakonfigurujte zdroj dat virtuální entity](#configure).

Další informace naleznete v tématu [Povolení integrace Microsoft Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Instalace virtuálních entit finance a provoz

Řešení Dataverse pro virtuální entity finance a provoz musí být nainstalovány pro řešení virtuální entity Microsoft AppSource.

1. V AppSource najděte [virtuální entitu financí a provozu](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Vyberte **Získat**.
3. V poli **Vybrat prostředí** zadejte hodnotu **Název prostředí**, kterou jste si poznamenali dříve.
4. Zaškrtněte políčka a poté vyberte **Nainstalovat**.

Po dokončení instalace můžete najít aplikaci **Virtuální entity financí a provozu** v [centru pro správu Power Platform](https://admin.powerplatform.microsoft.com/), pod **Zdroje** \> **Aplikace Dynamics 365**.

Další informace viz [Získání řešení virtuální entity](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Registrace aplikace Azure AD

Musíte zaregistrovat aplikaci Azure AD na stejném tenantovi jako finanční a provozní aplikace, aby je bylo možné volat z Dataverse.

1. V [portálu Azure](https://portal.azure.com) přejděte na **Azure Active Directory \> Registrace aplikací**.
2. Vyberte **Nová registrace** a poté zadejte následující informace:

    - **Název** – zadejte jedinečný název.
    - **Typ účtu** – Zadejte **Libovolný adresář Azure AD** (jeden tenant nebo více tenantů).
    - **Adresa URI pro přesměrování** – pole ponechejte prázdné.

3. Vyberte **Registrovat**.
4. Poznamenejte si hodnotu v poli **ID aplikace (klienta)**, protože ji budete potřebovat později.

    [![Hodnota ID aplikace Azure AD (klienta)](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Vytvořte symetrický klíč pro aplikaci.
6. V nové aplikaci vyberte **Certifikáty a tajné klíče**.
7. Vyberte **Nový tajný klíč klienta**.
8. Zadejte popis, vyberte datum vypršení platnosti a poté vyberte **Uložit**. Bude vytvořen a zobrazen klíč. Zkopírujte hodnotu pro pozdější použití.

Další informace naleznete v tématu [Registrace aplikace Azure AD](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>Udělení oprávnění finančním a provozním aplikacím

Dataverse používá aplikaci Azure AD, kterou jste vytvořili pro volání finančních a provozních aplikací. Aplikaci proto musí důvěřovat finanční a provozní aplikace a musí být přidružena k uživatelskému účtu, který má příslušná práva. Ve finančních a provozních aplikacích musíte vytvořit speciálního uživatele služby, který má práva **pouze** k funkčnosti virtuální entity. Tento uživatel služby nesmí mít žádná další práva. Po provedení tohoto kroku se každá aplikace, která má tajný klíč aplikace Azure AD, kterou jste vytvořili, bude moci volat prostředí finančních a provozních aplikací a přistupovat k funkcím virtuální entity.

1. V prostředí přejděte na **Správa systému** \> **Uživatelé** \> **Uživatelé**.
2. Vyberte **Nový** k přidání nového uživatele a zadejte následující informace:

    - **ID uživatele** – Zadejte **dataverseintegration** nebo jinou hodnotu.
    - **Uživatelské jméno** – Zadejte **integrace dataverse** nebo jinou hodnotu.
    - **Poskytovatel** – Nastavte toto pole na **NonAAD**.
    - **E-mail** – Zadejte **dataverseintegration** nebo jinou hodnotu. (Hodnota nemusí být platný e-mailový účet.)

3. Přiřaďte uživateli roli zabezpečení **Aplikace virtuální entity CDS**.
4. Odeberte všechny ostatní role, včetně **Uživatel systému**.
5. Přejděte do nabídky **Správa systému** \> **Nastavení** \> **Aplikace Azure Active Directory** pro registraci Dataverse. 
6. Přidejte řádek a poté v poli **ID klienta** zadejte hodnotu **ID aplikace (klienta)**, kterou jste si poznamenali dříve.
7. Do pole **Název** zadejte název. Například zadejte **Integrace Dataverse**.
8. Do pole **ID uživatele** zadejte ID uživatele, kterého jste dříve vytvořili.

Další informace naleznete [Udělení oprávnění aplikace ve finančních a provozních aplikacích](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Konfigurace zdroje dat virtuálních entit

Musíte Dataverse poskytnout instanci finančních a provozních aplikací, ke které se chcete připojit.

1. Prostředí Dataverse musí být ve vašem prohlížeči stále otevřené od [kroku 1. Aktivujte integraci Microsoft Power Platform a otevřete prostředí Dataverse](#enable). Vyberte tlačítko nastavení (symbol ozubeného kola) vpravo nahoře a poté vyberte položku **Pokročilá nastavení**.

    [![Otevření Pokročilých nastavení v prostředí Dataverse.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. V rozevírací nabídce **Nastavení** vyberte možnost **Správa**.

    [![Správa.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Vyberte **Zdroje dat virtuální entity**.

    [![Zdroje dat virtuální entity.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Vyberte zdroj dat s názvem **Finance a provoz**.

    [![Zdroj dat Finance a provoz.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Zadejte následující informace z předchozích kroků:

    - **Cílová adresa URL** – Zadejte adresu URL, ze které máte přístup k finančním a provozním aplikacím.
    - **Adresa URL protokolu OAuth** – Zadejte `https://login.windows.net/`.
    - **ID tenanta** – Zadejte tenanta. Tato hodnota může být název domény vašeho firemního e-mailu (například contoso.com).
    - **ID aplikace AAD** – Zadejte hodnotu **ID aplikace (klienta)**, kterou jste vytvořili dříve.
    - **Tajný klíč aplikace AAD** – Zadejte tajný klíč, který byl vygenerován dříve.
    - **Prostředek AAD** – Zadejte **00000015-0000-0000-c000-000000000000**. Tato hodnota je aplikace Azure AD, která představuje finanční a provozní aplikace. Měla by to být vždy stejná hodnota.

6. Uložte změny.
7. Zavřete stránku a vraťte se na stránku **Správa**, kde začnete [krok 6. Aktivujte virtuální entity Dataverse](#virtual).

    [![Zavření entity pro úpravy.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Další informace viz [Konfigurace zdroje dat virtuální entity](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Aktivace virtuálních entit Dataverse

Viditelnost virtuálních entit z finančních a provozních aplikací musí být nastavena na **Ano** dříve, než mohou být spotřebovány konfigurací Výpočet daně.

> [!NOTE]
> Tento krok můžete přeskočit tím, že povolíte virtuální entity související s výpočtem daně jediným kliknutím v [kroku 8. Nastavte připojenou aplikaci pro výpočet daně](#import). Doporučujeme však ručně povolit alespoň jednu virtuální entitu, abyste označili, že spojení mezi finančními a provozními aplikacemi a Dataverse je dobře zavedeno.

1. V prostředí Dataverse na stránce **Správa** vyberte tlačítko filtru (symbol trychtýře) v pravém horním rohu.

    [![Tlačítko Filtr.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. V okně **Pokročilé hledání** v poli **Hledat** vyberte **Dostupné finanční a provozní entity**.
3. Přidejte následující pravidlo: **Název** – **Obsahuje** – **CompanyInfoEntity**. Poté vyberte **Výsledky**.

    [![Okno pokročilého hledání.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Vyberte **CompanyInfoEntity** ve výsledcích vyhledávání, zaškrtněte políčko **Viditelné** a poté vyberte **Uložit**.

    [![Nastavení viditelnosti entity.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Opakujte předchozí kroky pro následující entity, na které se odkazuje v konfiguraci Výpočet daně:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Dataverse dokáže získat pouze prvních 5000 záznamů entity a zpřístupní se v rozevíracím seznamu konfigurace Výpočet daně.

Další informace viz [Povolení virtuálních entit Microsoft Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>Nastavte připojenou aplikaci pro výpočet daně

1. V RCS otevřete pracovní prostor **Správa funkcí** a zapněte následující funkce:

    - Podpora datových zdrojů Dataverse elektronického vykazování
    - Podpora datových zdrojů Dataverse daňové služby
    - Globalizační funkce

2. Přejděte na **Elektronické výkaznictví** v části **Související odkazy** vyberte **Propojené aplikace**.

    [![Připojené aplikace.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. Vyberte **Nový** k přidání záznamu a zadejte následující informace.

    - **Název** – Zadejte název.
    - **Typ** – Vyberte **Dataverse**.
    - **Aplikace** – Zadejte hodnotu **Adresa URL prostředí** prostředí Dataverse, kterou jste si poznamenali v [kroku 1. Aktivujte integraci Microsoft Power Platform a otevřete prostředí Dataverse](#enable).
    - **Tenant** – Zadejte tenanta.
    - **Vlastní adresa URL** – Zadejte adresu URL Dataverse a za ni napište **/api/data/v9.1**.

4. Vyberte **Zkontrolovat připojení** a poté v zobrazeném dialogovém okně vyberte **Kliknutím sem se připojíte k vybrané vzdálené aplikaci**.

    [![Kontrola připojení.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. Ujistěte se, že obdržíte zprávu „Úspěch!“, která označuje, že připojení bylo úspěšně navázáno.

    [![Zpráva o úspěchu.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Importujte a nastavte konfiguraci mapování modelu Dataverse

Společnost Microsoft poskytuje výchozí konfigurace mapování modelu pro entity z finančních a provozních aplikací po výpočet daně.

1. V RCS přejděte na **Elektronické sestavy**.
2. V části **Poskytovatelé konfigurace** na dlaždici pro poskytovatele konfigurace **Microsoft** vyberte **Úložiště**.

    [![Úložiště.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Vyberte záznam **Úložiště globální konfigurace** a pak vyberte možnost **Otevřít**.
4. V části **Daňový datový model** \> **Datový model výpočtu daně** vyberte konfiguraci **Mapování modelu Dataverse**.
5. Na pevné záložce **Verze** vyberte verzi, která odpovídá verzi vaší finanční a provozní aplikace, a poté vyberte **Importovat**.

    [![Importování konfigurace mapování modelu Dataverse.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Konfigurace **Mapování modelu Dataverse** je účinná pouze na nejvyšší importované verzi. Proto byste neměli importovat verzi konfigurace **Mapování modelu Dataverse**, která je vyšší než verze konfigurace Výpočet daně, kterou plánujete implementovat. Pokud například plánujete implementovat verzi 40.50.225 konfigurace výpočtu daně, měli byste importovat pouze verzi 40.50.13 konfigurace **Mapování modelu Dataverse**. Neměli byste importovat verzi 40.54.14. V opačném případě dojde v konfiguraci k nesouladu datového modelu.

6. Přejděte do pracovního prostoru **Elektronické výkaznictví** a vyberte dlaždici **Konfigurace daní**.
7. Vyberte importovanou konfiguraci **Mapování modelu Dataverse** a poté vyberte **Upravit**.
8. Nastavte možnost **Výchozí pro mapování modelu’** na **Ano**.
9. V poli **Připojená aplikace** vyberte připojenou aplikaci, kterou jste nastavili v [kroku 7. Nastavte připojenou aplikaci pro výpočet daně](#set-up).
10. Nastavte možnost **Nastavit viditelnost virtuální tabulky** na **Ano** pro nastavení všech virtuálních entit souvisejících s výpočtem daně jako viditelných.

Nyní jste dokončili nastavení funkce vyhledávání hlavních dat. Rozbalovací seznam pro pole jako např. **Právnická osoba**, **Účet dodavatele**, **Kód položky** a **Termín doručení** z Dynamics 365 Finance bude nyní aktivován v nastavení **Verze funkce výpočtu daně**.

[![Rozbalovací seznam právnických osob.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
