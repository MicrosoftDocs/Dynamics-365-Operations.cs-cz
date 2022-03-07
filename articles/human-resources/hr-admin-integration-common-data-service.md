---
title: Konfigurovat integraci se službou Dataverse
description: Integraci mezi Microsoft Dataverse a Dynamics 365 Human Resources můžete zapnout nebo vypnout. Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat tabulku.
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 721799c9a6fafe0a809f447189ce6814b30ca863
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052450"
---
# <a name="configure-dataverse-integration"></a>Konfigurovat integraci se službou Dataverse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Integraci mezi Microsoft Dataverse a Dynamics 365 Human Resources můžete zapnout nebo vypnout. Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat tabulku.

> [!NOTE]
> Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Když vypnete integraci, uživatelé mohou provádět změny v Human Resources nebo Dataverse, ale tyto změny se mezi oběma prostředími nesynchronizují.

Ve výchozím nastavení je integrace dat mezi Human Resources a Dataverse vypnuta.

V těchto situacích je vhodné vypnout integraci:

- Vyplňujete data prostřednictvím Data Management Framework a je nutné je importovat vícekrát, aby je bylo možné dostat do správného stavu.

- Existují problémy s daty v modulu Human Resources nebo Dataverse. Pokud vypnete integraci, můžete odstranit záznam v jednom prostředí, aniž byste ho odstranili v jiném. Pokud opět zapnete integraci, bude záznam v prostředí, kde nebyl odstraněn, synchronizován zpět do prostředí, ve kterém byl odstraněn. Synchronizace začíná při příštím spuštění dávkové úlohy **Integrace Dataverse zmeškala synchronizaci požadavku**.

> [!WARNING]
> Když vypnete integraci dat, ujistěte se, že neupravujete stejný záznam v obou prostředích. Pokud zapnete integraci znovu, bude naposledy upravený záznam synchronizován. Pokud tedy neprovedete stejné změny v záznamu v obou prostředích, může dojít ke ztrátě dat.

## <a name="access-the-dataverse-integration-page"></a>Přístup na stránku integrace Dataverse

1. V instanci Human Resources, v níž chcete zobrazit nebo konfigurovat nastavení pro integraci s Dataverse, vyberte dlaždici **Správa systému**.

    [![Dlaždice správy systému](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Zvolte kartu **Odkazy**.

    [![Karta Odkazy](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. V části **Integrace** vyberte **Konfigurace Dataverse**.

    [![Odkaz na konfiguraci Dataverse](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Zapnutí a vypnutí integrace dat mezi Human Resources a Dataverse

- Chcete-li zapnout integraci, nastavte možnost **Povolit integraci Dataverse** na stránce **Integrace doMicrosoft Dataverse** na **Ano**.

    > [!NOTE]
    > Při zapnutí integrace budou data synchronizována při příštím spuštění dávkové úlohy **Integrace Dataverse zmeškala synchronizaci požadavku**. Všechna data by měla být k dispozici po dokončení dávkové úlohy.

- Chcete-li vypnout integraci, nastavte možnost na **Ne**.

[![Zapnutí a vypnutí integrace Dataverse](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Důrazně doporučujeme vypnout integraci Dataverse při provádění úkolů migrace dat. Odesílání velkého objemu dat může výrazně ovlivnit výkon. Například nahrávání 2000 pracovníků může trvat několik hodin, když je integrace povolena, a méně než jednu hodinu, pokud je zakázána. Čísla uvedená v tomto příkladu slouží pouze k demonstračním účelům. Přesné množství času potřebného k importu záznamů se může značně lišit v závislosti na mnoha faktorech.

## <a name="view-data-integration-details"></a>Zobrazení podrobností integrace dat

Na záložce s náhledem **Správa** na stránce **Integrace Microsoft Dataverse** můžete zobrazit, jak budou řádky vzájemně propojeny mezi Human Resources a Dataverse.

- Chcete-li zobrazit řádky tabulky, vyberte tabulku v poli **Tabulky Dataverse**. V mřížce jsou uvedeny všechny řádky, které jsou propojeny s vybranou tabulkou.

> [!NOTE]
> V tuto chvíli nejsou uvedeny všechny tabulky Dataverse. V mřížce se zobrazí pouze tabulky, které podporují použití vlastních polí. Nové tabulky jsou k dispozici prostřednictvím kontinuálního vydávání aplikace Human Resources.

Mřížka obsahuje následující pole:

- **Tabulka Dataverse** - Název tabulky v Dataverse.
- **Odkaz na Dataverse tabulku**- identifikátor používající Dataverse k identifikaci záznamu. Tato hodnota je ekvivalentní hodnotě **RecId** Human Resources. Identifikátor lze najít při otevření tabulky Dataverse v aplikaci Microsoft Excel.
- **Název entity Human Resources** – entita Human Resources, která naposledy synchronizovala data do Dataverse. Entita může mít buď předponu Dataverse, nebo jinou předponu.
- **Odkaz na Human Resources** - hodnota **RecId**, která je přidružená k záznamu v Human Resources.
- **Odstraněna z Dataverse** - hodnota, která určuje, zda byl řádek odstraněn z Dataverse.

> [!NOTE]
> Záznamy v Human Resources odpovídají řádkům v Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Odebrání přidružení záznamu v Human Resources z řádku Dataverse

Pokud se setkáte s problémy při synchronizaci dat mezi Human Resources a Dataverse, můžete je vyřešit vymazáním sledování a opakovanou synchronizací sledovací tabulky. Pokud přidružení odeberete a poté změníte nebo odstraníte řádek v Dataverse, nebudou provedené změny synchronizovány do Human Resources. Pokud provedete změny v Human Resources, bude vytvořen nový záznam sledování a řádek bude aktualizován v Dataverse.

- Chcete-li odebrat přidružení záznamu mezi záznamem a řádkem Dataverse v Human Resources, vyberte **Tabulka Dataverse** a poté vyberte možnost **Vymazat informace o sledování**.

[![Vymazat informace o sledování](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Chcete-li spustit úplnou synchronizaci tabulky po vymazání sledování, postupujte podle následujícího postupu.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Synchronizace tabulky mezi Human Resources a Dataverse

Tento postup použijte v následujících případech:

- Zobrazení změn Dataverse v Human Resources trvá příliš dlouho.

- Chcete-li sledování vymazat, je nutné aktualizovat sledovací tabulku.

Chcete-li spustit úplnou synchronizaci tabulky mezi Human Resources a Dataverse:

1. Vyberte tabulku v poli **Tabulka Dataverse**.

2. Vyberte **Synchronizovat nyní**.

[![Spuštění úplné synchronizace](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Viz také

[Tabulky Dataverse](hr-developer-entities.md)<br>
[Konfigurace virtuálních tabulek Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Virtuální tabulky lidských zdrojů - časté dotazy](hr-admin-virtual-entity-faq.md)<br>
[Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Aktualizace terminologie](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]