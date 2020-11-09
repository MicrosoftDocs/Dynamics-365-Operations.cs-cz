---
title: Konfigurace virtuálních entit Common Data Service
description: Toto téma ukazuje, jak konfigurovat virtuální entity pro Dynamics 365 Human Resources. Můžete generovat a aktualizovat existující virtuální entity a analyzovat vygenerované a dostupné entity.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058147"
---
# <a name="configure-common-data-service-virtual-entities"></a>Konfigurace virtuálních entit Common Data Service

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources je virtuální zdroj dat v Common Data Service. Poskytuje úplné operací vytváření, čtení, aktualizace a mazání (CRUD) z Common Data Service a Microsoft Power Platform. Data pro virtuální entity nejsou uloženy v Common Data Service, ale v databázi aplikace. 

Pro povolení operací CRUD v entitách Human Resources z Common Data Service musíte entity zpřístupnit jako virtuální entity v Common Data Service. To vám umožní provádět operace CRUD z Common Data Service a Microsoft Power Platform na datech v Human Resources. Operace také podporují úplné ověření obchodní logiky Human Resources, aby byla zajištěna integrita dat při jejich zápisu do entit.

## <a name="available-virtual-entities-for-human-resources"></a>Dostupné virtuální entity pro Human Resources

Všechny entity Open Data Protocol (OData) v Human Resources jsou k dispozici jako virtuální entity v Common Data Service. Jsou k dispozici i v Power Platform. Nyní můžete vytvářet aplikace a prostředí s daty přímo z Human Resources s plnou schopností CRUD, a to bez kopírování nebo synchronizace dat do Common Data Service. Můžete používat portály Power Apps k vytváření externích webů, které umožňují scénáře spolupráce pro obchodní procesy v Human Resources.

Můžete zobrazit seznam virtuálních entit povolených v prostředí a začít pracovat s entitami v [Power Apps](https://make.powerapps.com), v řešení **Virtuální entity Dynamics 365 HR**.

![Virtuální entity Dynamics 365 HR ve Windows Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuální entity versus přirozené entity

Virtuální entity pro Human Resources nejsou totéž jako přirozené entity Common Data Service vytvořené pro Human Resources. Přirozené entity pro Human Resources jsou generovány samostatně a udržovány v řešení HCM Common v Common Data Service. U přirozených entit jsou data uložena v Common Data Service a vyžaduje synchronizaci s databází aplikace Human Resources.

> [!NOTE]
> Seznam přirozených entit Common Data Service pro Human Resources viz [Entity Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Nastavení

Povolte virtuální entity ve vašem prostředí provedením těchto kroků nastavení. 

### <a name="register-the-app-in-microsoft-azure"></a>Registrace aplikace v Microsoft Azure

Nejprve musíte zaregistrovat aplikaci na webu Azure Portal, aby platforma identit od Microsoftu mohla poskytovat ověřovací a autorizační služby pro tuto aplikaci a uživatele. Další informace o registraci aplikací v Azure najdete v tématu [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Otevřete [Microsoft Azure Portal](https://portal.azure.com).

2. V seznamu služeb Azure zvolte **Registrace aplikací**.

3. Vyberte **Nová registrace**.

4. V poli **Název** zadejte popisný název aplikace. Například **Virtuální entity Dynamics 365 Human Resources**.

5. V poli **URI přesměrování** zadejte adresu URL oboru názvů vaší instance Human Resources.

6. Vyberte **Registrovat**.

7. Po dokončení registrace se na webu Azure Portal zobrazí podokno **Přehled** pro registraci aplikace, které obsahuje jeho **ID aplikace (klienta)**. V tuto chvíli si **ID aplikace (klienta)** poznamenejte. Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních entit](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. V levém navigačním podokně vyberte **Certifikáty a tajné klíče**.

9. V části **Tajné klíče klienta** stránky vyberte **Nový tajný klíč klienta**.

10. Zadejte popis, vyberte dobu trvání a vyberte **Přidat**.

11. Zaznamenejte hodnotu tajného klíče. Tyto informace zadáte, až budete [konfigurovat zdroj dat virtuálních entit](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > V tuto chvíli si nezapomeňte hodnotu tajného klíče poznamenat. Po opuštění této stránky se tajný klíč už nikdy nezobrazí.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Instalace aplikaci Dynamics 365 HR Virtual Entity

Nainstalujte si aplikaci Dynamics 365 HR Virtual Entity do svého prostředí Power Apps, abyste si nasadili balíček řešení virtuální entity do Common Data Service.

1. Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2. V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.

3. V části **Zdroje** této stránky vyberte **Aplikace Dynamics 365**.

4. Vyberte akci **Nainstalovat aplikaci**.

5. Vyberte **Dynamics 365 HR Virtual Entity** a pak **Další**.

6. Přečtěte si podmínky služby a potvrďte svůj souhlas.

7. Vyberte **Instalovat**.

Instalace trvá několik minut. Po jejím dokončení pokračujte dalšími kroky.

![Instalace aplikace Dynamics 365 HR Virtual Entity z centra pro správu Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Konfigurace zdroje dat virtuálních entit 

Dalším krokem je konfigurace zdroje dat virtuálních entit v prostředí Power Apps. 

1. Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2. V seznamu **Prostředí** vyberte prostředí Power Apps spojené s vaší instancí Human Resources.

3. Vyberte **URL prostředí** v části **Podrobnosti** této stránky.

4. V **Centru stavu řešení** vyberte ikonu **Rozšířené hledání** v pravém horním rohu stránky aplikace.

5. Na stránce **Rozšířené hledání** vyberte v rozevíracím seznamu **Hledat** položku **Konfigurace zdrojů virtuálních dat ve Finance and Operations**.

6. Vyberte **Výsledky**

7. Vyberte záznam **Zdroj dat Microsoft HR**.

8. Zadejte požadované informace pro konfiguraci zdroje dat.

   - **Cílová adresa URL** : URL vašeho oboru názvů pro Human Resources.
   - **ID tenanta** : ID tenanta Azure Active Directory (Azure AD).
   - **ID aplikace AAD** : ID aplikace (klienta) vytvořené pro aplikaci registrovanou přes Microsoft Azure Portal. Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).
   - **Tajný klíč aplikace AAD** : Tajný klíč klienta vytvořený pro aplikaci registrovanou přes Microsoft Azure Portal. Tyto informace jste obdrželi dříve v rámci kroku [Registrace aplikace v Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

9. Zvolte **Uložit a zavřít**.

   ![Zdroj dat Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Udělení oprávnění aplikací v Human Resources

Udělte oprávnění těmto dvěma aplikacím Azure AD v oblasti Human Resources:

- Aplikace vytvořená pro vašeho tenanta přes Microsoft Azure Portal
- Aplikace Dynamics 365 HR Virtual Entity nainstalovaná v prostředí Power Apps 

1. V Human Resources otevřete stránku **Aplikace Azure Active Directory**.

2. Zvolte **Nový** pro vytvoření nového záznamu aplikace:

    - V poli **ID klienta** zadejte ID klienta aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.
    - V poli **Název** zadejte název aplikace, kterou jste zaregistrovali přes Microsoft Azure Portal.
    - V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.

3. Zvolte **Nový** pro vytvoření druhého záznamu aplikace:

    - **ID klienta** : f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Název** : Dynamics 365 HR Virtual Entity
    - V poli **ID uživatele** vyberte ID uživatele s oprávněními správce v Human Resources a prostředí Power Apps.

## <a name="generate-virtual-entities"></a>Generování virtuálních entit

Po dokončení instalace můžete vybrat virtuální entity, které chcete vygenerovat a povolit ve vaší instanci Common Data Service.

1. V Human Resources otevřete stránku **Integrace Common Data Service (CDS)**.

2. Vyberte kartu **Virtuální entity**.

> [!NOTE]
> Přepínač **Povolte virtuální entitu** bude nastaven na **Ano** automaticky po dokončení všech požadovaných nastavení. Pokud je přepínač nastaven na **Ne** , zkontrolujte kroky v předchozích částech tohoto dokumentu a ujistěte se, že jsou dokončeny všechny nezbytné předpoklady.

3. Vyberte entitu nebo entity, které chcete generovat v Common Data Service.

4. Vyberte **Generovat/aktualizovat**.

![Integrace Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Zkontrolujte stav generování entity

Virtuální entity jsou generovány v Common Data Service prostřednictvím asynchronního procesu na pozadí. Aktualizace na displeji procesu v centru akcí. Podrobnosti o procesu, včetně protokolů chyb, se objeví na stránce **Procesní automatizace**.

1. V Human Resources otevřete stránku **Procesní automatizace**.

2. Vyberte kartu **Procesy na pozadí**.

3. Vyberte **Proces na pozadí asynchronní operace s dotazováním virtuální entity**.

4. Vyberte **Zobrazit nejnovější výsledky**.

V posuvném podokně se zobrazují nejnovější výsledky provádění procesu. Můžete zobrazit protokol procesu, včetně všech chyb vrácených z Common Data Service.

## <a name="see-also"></a>Viz také

[Co je Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Přehled entit](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Přehled vztahů mezi entitami](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Vytváření a úpravy virtuálních entit, které obsahují data z externího zdroje dat](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Co jsou portály Power Apps?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Přehled vytváření aplikací v Power Apps](https://docs.microsoft.com/powerapps/maker/)
