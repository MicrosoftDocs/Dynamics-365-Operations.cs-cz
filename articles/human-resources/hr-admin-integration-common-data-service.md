---
title: Konfigurace integrace Common Data Service
description: Integraci mezi Common Data Service a instanci Microsoft Dynamics 365 Human Resources můžete zapnout nebo vypnout. Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat entitu.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008328"
---
# <a name="configure-common-data-service-integration"></a>Konfigurace integrace Common Data Service

Integraci mezi Common Data Service a instanci Microsoft Dynamics 365 Human Resources můžete zapnout nebo vypnout. Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat entitu.

Když vypnete integraci, uživatelé mohou provádět změny v Human Resources nebo Common Data Service, ale tyto změny se mezi oběma prostředími nesynchronizují.

Ve výchozím nastavení je integrace mezi Human Resources a Common Data Service vypnuta nebo zapnuta, v závislosti na přítomnosti ukázkových dat v prostředí:

- **Vypnuta** pro nová prostředí, která nezahrnují ukázková data
- **Zapnuta** pro nová prostředí, která zahrnují ukázková data

Nová prostředí, která zahrnují ukázková data, začnou synchronizovat data při jejich zřizování.

V těchto situacích je vhodné vypnout integraci:

- Vyplňujete data prostřednictvím Data Management Framework a je nutné je importovat vícekrát, aby je bylo možné dostat do správného stavu.

- Existují problémy s daty v modulu Human Resources nebo Common Data Service. Pokud vypnete integraci, můžete odstranit záznam v jednom prostředí, aniž byste ho odstranili v jiném. Pokud opět zapnete integraci, bude záznam v prostředí, kde nebyl odstraněn, synchronizován zpět do prostředí, ve kterém byl odstraněn. Synchronizace začíná při příštím spuštění dávkové úlohy **Integrace Common Data Service zmeškala synchronizaci požadavku**.

> [!WARNING]
> Když vypnete integraci dat, ujistěte se, že neupravujete stejný záznam v obou prostředích. Pokud zapnete integraci znovu, bude naposledy upravený záznam synchronizován. Pokud tedy neprovedete stejné změny v záznamu v obou prostředích, může dojít ke ztrátě dat.

## <a name="access-the-common-data-service-integration-page"></a>Přístup na stránku integrace Common Data Service

1. V instanci Human Resources, v níž chcete zobrazit nebo konfigurovat nastavení pro integraci s Common Data Service, vyberte dlaždici **Správa systému**.

    [![Dlaždice správy systému](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Zvolte kartu **Odkazy**.

    [![Karta Odkazy](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. V části **Integrace** vyberte **Konfigurace Common Data Service**.

    [![Odkaz na konfiguraci Common Data Service](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Zapnutí a vypnutí integrace dat mezi Human Resources a Common Data Service

- Chcete-li zapnout integraci, nastavte možnost **Povolit integraci do Common Data Service** na **Ano**.

    > [!NOTE]
    > Při zapnutí integrace budou data synchronizována při příštím spuštění dávkové úlohy **Integrace Common Data Service zmeškala synchronizaci požadavku**. Všechna data by měla být k dispozici po dokončení dávkové úlohy.

- Chcete-li vypnout integraci, nastavte možnost na **Ne**.

[![Zapnutí a vypnutí integrace Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Zobrazení podrobností integrace dat

Na záložce s náhledem **Správa** na stránce **Integrace Common Data Service** můžete zobrazit, jak budou záznamy vzájemně propojeny mezi Human Resources a Common Data Service.

- Chcete-li zobrazit záznamy pro entitu, vyberte entitu v poli **Název entity CDS**. V mřížce jsou uvedeny všechny záznamy, které jsou propojeny s vybranou entitou.

[![Zobrazení záznamů entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> V tuto chvíli nejsou uvedeny všechny entity Common Data Service. V mřížce se zobrazí pouze entity, které podporují použití vlastních polí. Nové entity jsou k dispozici prostřednictvím kontinuálního vydávání aplikace Human Resources.

Mřížka obsahuje následující pole:

- **Název entity CDS** - název entity v Common Data Service.
- **Odkaz entity CDS**- identifikátor používající Common Data Service k identifikaci záznamu. Tato hodnota je ekvivalentní hodnotě **RecId** Human Resources. Identifikátor lze najít při otevření entity Common Data Service v aplikaci Microsoft Excel.
- **Název entity Human Resources** – entita, která naposledy synchronizovala data do Common Data Service. Entita může mít buď předponu Common Data Service, nebo jinou předponu.
- **Odkaz na Human Resources** - hodnota **RecId**, která je přidružená k záznamu v Human Resources.
- **Byla odstraněna z CDS** – hodnota, která určuje, zda byl záznam odstraněn z Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Odebrání přidružení záznamu v Human Resources z Common Data Service

Pokud se setkáte s problémy při synchronizaci dat mezi Human Resources a Common Data Service, můžete je vyřešit vymazáním sledování a opakovanou synchronizací sledovací tabulky. Pokud přidružení odeberete a poté změníte nebo odstraníte záznam v Common Data Service, nebudou provedené změny synchronizovány do Human Resources. Pokud provedete změny v Human Resources, bude vytvořen nový záznam sledování a záznam bude aktualizován v Common Data Service.

- Chcete-li odebrat přidružení záznamu mezi Human Resources. a Common Data Service, vyberte entitu v poli **Název entity CDS** a poté vyberte možnost **Vymazat informace o sledování**.

[![Vymazat informace o sledování](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Chcete-li spustit úplnou synchronizaci entity po vymazání sledování, postupujte podle následujícího postupu.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Synchronizace entity mezi Human Resources a Common Data Service

Tento postup použijte v případě, že změnám z Common Data Service trvá příliš dlouho, než se projeví v Human Resources, nebo pokud je nutné aktualizovat tabulku sledování po vymazání sledování.

- Chcete-li spustit úplnou synchronizaci entity mezi Human Resources a Common Data Service, vyberte entitu v poli **Název entity CDS** a pak vyberte **Synchronizovat nyní**.

[![Spuštění úplné synchronizace](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)

