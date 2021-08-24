---
title: Konfigurace virtuálních tabulek Dataverse
description: Toto téma ukazuje, jak konfigurovat virtuální tabulky pro Dynamics 365 Human Resources. Můžete generovat a aktualizovat existující virtuální tabulky a analyzovat vygenerované a dostupné tabulky.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4461b072c12848220c48d3a711cc2d4991c98f068e1ba477becf6d0be068fca8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721600"
---
# <a name="configure-dataverse-virtual-tables"></a>Konfigurace virtuálních tabulek Dataverse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources je virtuální zdroj dat v Microsoft Dataverse. Poskytuje úplné operací vytváření, čtení, aktualizace a mazání (CRUD) z Dataverse a Microsoft Power Platform. Data pro virtuální tabulky nejsou uloženy v Dataverse, ale v databázi aplikace.

Pro povolení operací CRUD v entitách Human Resources z Dataverse musíte entity zpřístupnit jako virtuální tabulky v Dataverse. To vám umožní provádět operace CRUD z Dataverse a Microsoft Power Platform na datech v Human Resources. Operace také podporují úplné ověření obchodní logiky Human Resources, aby byla zajištěna integrita dat při jejich zápisu do entit.

> [!NOTE]
> Entity Human Resources odpovídají Dataverse tabulkám. Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Dostupné virtuální tabulky pro Human Resources

Všechny entity Open Data Protocol (OData) v Human Resources jsou k dispozici jako virtuální tabulky v Dataverse. Jsou k dispozici i v Power Platform. Nyní můžete vytvářet aplikace a prostředí s daty přímo z Human Resources s plnou schopností CRUD, a to bez kopírování nebo synchronizace dat do Dataverse. Můžete používat portály Power Apps k vytváření externích webů, které umožňují scénáře spolupráce pro obchodní procesy v Human Resources.

Můžete zobrazit seznam virtuálních tabulek povolených v prostředí a začít pracovat s tabulkami v [Power Apps](https://make.powerapps.com), v řešení **Virtuální tabulky Dynamics 365 HR**.

![Virtuální tabulky Dynamics 365 HR v Power Apps.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuální tabulky versus nativní tabulky

Virtuální tabulky pro Human Resources nejsou totéž jako nativni tabulky Dataverse vytvořené pro Human Resources. 

Nativní tabulky pro Human Resources jsou generovány samostatně a udržovány v řešení HCM Common v Dataverse. U nativních tabulek jsou data uložena v Dataverse a vyžaduje synchronizaci s databází aplikace Human Resources.

> [!NOTE]
> Seznam nativních tabulek Dataverse pro Human Resources viz [Tabulky Dataverse](./hr-developer-entities.md).

## <a name="setup"></a>Nastavení

Povolte virtuální tabulky ve vašem prostředí provedením těchto kroků nastavení.

### <a name="enable-virtual-tables-in-human-resources"></a>Povolení virtuálních tabulek v Human Resources

Nejprve musíte povolit virtuální tabulky v pracovním prostoru **Správa funkcí**.

1. V modulu Human Resources vyberte **Správa systému**.

2. Vyberte dlaždici **Správa funkcí**.

3. Vyberte **Podpora virtuálních tabulek v HR v Dataverse** a potom vyberte **Povolit**.

Další informace o povolení a zákazu funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Registrace aplikace v Microsoft Azure

Musíte registrovat instanci Human Resources v portálu Azure, aby platforma identit od Microsoftu mohla poskytovat ověřovací a autorizační služby pro tuto aplikaci a uživatele. Další informace o registraci aplikací v Azure najdete v tématu [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](/azure/active-directory/develop/quickstart-register-app).

1. Otevřete [Microsoft Azure Portal](https://portal.azure.com).

2. V seznamu služeb Azure zvolte **Registrace aplikací**.

3. Vyberte **Nová registrace**.

4. V poli **Název** zadejte popisný název aplikace. Například **Virtuální tabulky Dynamics 365 Human Resources**.

5. V poli **URI přesměrování** zadejte adresu URL oboru názvů vaší instance Human Resources.

6. Vyberte **Registrovat**.

7. Po dokončení registrace se na webu Azure Portal zobrazí podokno **Přehled** pro registraci aplikace, které obsahuje jeho **ID aplikace (klienta)**. V tuto chvíli si **ID aplikace (klienta)** poznamenejte. Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních tabulek](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. V levém navigačním podokně vyberte **Certifikáty a tajné klíče**.

9. V části **Tajné klíče klienta** stránky vyberte **Nový tajný klíč klienta**.

10. Zadejte popis, vyberte dobu trvání a vyberte **Přidat**.

11. Zaznamenejte hodnotu tajného klíče z vlastnosti **Hodnota** tabulky. Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních tabulek](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > V tuto chvíli si nezapomeňte hodnotu tajného klíče poznamenat. Po opuštění této stránky se tajný klíč už nikdy nezobrazí.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Instalace aplikaci Dynamics 365 HR Virtual Table

Nainstalujte si aplikaci Dynamics 365 HR Virtual Table do svého prostředí Power Apps, abyste si nasadili balíček řešení virtuální tabulky do Dataverse.

1. V Human Resources otevřete stránku **Integrace Microsoft Dataverse**.

2. Vyberte kartu **Virtuální tabulky**.

3. Vyberte **Nainstalovat aplikaci virtuální tabulky**.

### <a name="configure-the-virtual-table-data-source"></a>Konfigurace zdroje dat virtuálních tabulek

Dalším krokem je konfigurace zdroje dat virtuálních tabulek v prostředí Power Apps.

1. Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2. V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.

3. Vyberte **URL prostředí** v části **Podrobnosti** této stránky.

4. V **Centru stavu řešení** vyberte ikonu **Rozšířené hledání** v pravém horním rohu stránky aplikace.

5. Na stránce **Rozšířené hledání** vyberte v rozevíracím seznamu **Hledat** položku **Konfigurace zdrojů virtuálních dat ve Finance and Operations**.

   > [!NOTE]
   > Instalace aplikace virtuální tabulky z předchozího kroku instalace může trvat několik minut. Pokud **Konfigurace virtuálního datového zdroje Finance and Operations** nejsou k dispozici v seznamu, počkejte minutu a obnovte seznam.

6. Vyberte **Výsledky**

7. Vyberte záznam **Zdroj dat Microsoft HR**.

8. Zadejte požadované informace pro konfiguraci zdroje dat:

   - **Cílová adresa URL**: URL vašeho oboru názvů pro Human Resources. Formát cílové adresy URL je:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Například:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Nezapomeňte uvést znak „**/**“ na konci adresy URL, aby nedošlo k chybě.

   - **ID tenanta**: ID tenanta Azure Active Directory (Azure AD).

   - **ID aplikace AAD**: ID aplikace (klienta) vytvořené pro aplikaci registrovanou přes Microsoft Azure Portal. Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **Tajný klíč aplikace AAD**: Tajný klíč klienta vytvořený pro aplikaci registrovanou přes Microsoft Azure Portal. Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Zdroj dat Microsoft HR.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Zvolte **Uložit a zavřít**.

### <a name="grant-app-permissions-in-human-resources"></a>Udělení oprávnění aplikací v Human Resources

Udělte oprávnění těmto dvěma aplikacím Azure AD v oblasti Human Resources:

- Aplikace vytvořená pro vašeho tenanta přes Microsoft Azure Portal
- Aplikace Dynamics 365 HR Virtual Table nainstalovaná v prostředí Power Apps 

1. V Human Resources otevřete stránku **Aplikace Azure Active Directory**.

2. Zvolte **Nový** pro vytvoření nového záznamu aplikace:

    - V poli **ID klienta** zadejte ID klienta aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.
    - V poli **Název** zadejte název aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.
    - V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.

3. Zvolte **Nový** pro vytvoření druhého záznamu aplikace:

    - **ID klienta**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Název**: Dynamics 365 HR Virtual Table
    - V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.

## <a name="generate-virtual-tables"></a>Generování virtuálních tabulek

Po dokončení instalace můžete vybrat virtuální tabulku, které chcete vygenerovat a povolit ve vaší instanci Dataverse.

1. V Human Resources otevřete stránku **Integrace Microsoft Dataverse**.

2. Vyberte kartu **Virtuální tabulky**.

> [!NOTE]
> Přepínač **Povolte virtuální tabulku** bude nastaven na **Ano** automaticky po dokončení všech požadovaných nastavení. Pokud je přepínač nastaven na **Ne**, zkontrolujte kroky v předchozích částech tohoto dokumentu a ujistěte se, že jsou dokončeny všechny nezbytné předpoklady.

3. Vyberte tabulku nebo tabulku, kterou chcete generovat v Dataverse.

4. Vyberte **Generovat/aktualizovat**.

![Integrace Dataverse.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Zkontrolujte stav generování tabulky

Virtuální tabulky jsou generovány v Dataverse prostřednictvím asynchronního procesu na pozadí. Aktualizace na displeji procesu v centru akcí. Podrobnosti o procesu, včetně protokolů chyb, se objeví na stránce **Procesní automatizace**.

1. V Human Resources otevřete stránku **Procesní automatizace**.

2. Vyberte kartu **Procesy na pozadí**.

3. Vyberte **Proces na pozadí asynchronní operace s dotazováním virtuální tabulky**.

4. Vyberte **Zobrazit nejnovější výsledky**.

V posuvném podokně se zobrazují nejnovější výsledky provádění procesu. Můžete zobrazit protokol procesu, včetně všech chyb vrácených z Dataverse.

## <a name="see-also"></a>Viz také

[Co je Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Tabulky v Dataverse](/powerapps/maker/common-data-service/entity-overview)<br>
[Přehled vztahů mezi tabulkami](/powerapps/maker/common-data-service/relationships-overview)<br>
[Vytváření a úpravy virtuálních tabulek, které obsahují data z externího zdroje dat](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Co jsou portály Power Apps?](/powerapps/maker/portals/overview)<br>
[Přehled vytváření aplikací v Power Apps](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
