---
title: Integrace správy majetku s dlouhodobým majetkem
description: V tomto tématu je vysvětleno, jak integrovat moduly Správa majetku a Dlouhodobý majetek tak, aby bylo možné propojit dlouhodobý majetek s objekty údržby.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423704"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Integrace správy majetku s dlouhodobým majetkem

[!include [banner](../../includes/banner.md)]

Integrací modulů **Správa majetku** a **Dlouhodobý majetek** můžete propojit dlouhodobý majetek s objekty údržby. Uživatelé modulu Dlouhodobý majetek pak mohou vytvořit objekt údržby z nového nebo existujícího dlouhodobého majetku a uživatelé modulu Správa majetku mohou k existujícímu dlouhodobému majetku přidružit objekt údržby. Tato funkce rovněž usnadňuje uživatelům modulu Dlouhodobý majetek zobrazení nákladů, které byly zaúčtovány z pracovních příkazů pro související objekty údržby.

> [!NOTE]
> V tomto tématu *objekty údržby* odkazují na majetek z modulu **Správa majetku** a *dlouhodobý majetek* na majetek z modulu **Dlouhodobý majetek**.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Nastavení výchozího umístění pro nové objekty údržby vytvořené z dlouhodobého majetku (volitelné)

Tato volitelná konfigurace vám umožňuje nastavit výchozí umístění pro nové objekty údržby vytvořené z dlouhodobého majetku. Tuto konfiguraci obvykle provedete pouze jednou, pokud ji vůbec provedete.

Konfiguraci provedete následovně:

1. Přejděte do nabídky **Správa majetku \> Nastavení \> Parametry správy skladu**.
1. Na kartě **Dlouhodobý majetek** v poli **Funkční místo** vyberte výchozí umístění.
1. V podokně akcí vyberte **Uložit**.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Práce s integrovanými objekty údržby a dlouhodobým majetkem

Tato část obsahuje kolekci postupů, které představují různé způsoby práce s integrovanými funkcemi správy majetku a dlouhodobého majetku.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Přidružení existujícího objektu údržby k dlouhodobému majetku

Chcete-li přidružit existující objektu údržby k dlouhodobému majetku, postupujte následovně.

1. Přejděte na **Správa majetku \> Majetek \> Všechen majetek** (nebo **Aktivní majetek**).
1. Vyberte majetek.
1. Na záložce s náhledem **Dlouhodobý majetek** v poli **Číslo dlouhodobého majetku** vyberte existující dlouhodobý majetek.
1. V podokně akcí vyberte **Uložit**.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Zobrazení dlouhodobého majetku, který je přidružen k vybranému objektu údržby

Chcete-li zobrazit dlouhodobý majetek, který je přidružen k vybranému objektu údržby, postupujte podle následujících kroků.

1. Přejděte na **Správa majetku \> Majetek \> Všechen majetek** (nebo **Aktivní majetek**).
1. Vyberte majetek.
1. Na záložce s náhledem **Dlouhodobý majetek** v poli **Číslo dlouhodobého majetku** vyberte odkaz.

    Otevře se stránka **Dlouhodobý majetek** pro vybraný majetek. (Tato stránka se obvykle nachází v umístění **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Zobrazení objektu údržby, který je přidružen k vybranému dlouhodobému majetku

Chcete-li zobrazit objekt údržby, který je přidružen k vybranému dlouhodobému majetku, postupujte podle následujících kroků.

1. Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.
1. Vyberte majetek.
1. V podokně akcí na kartě **Správa majetku** ve skupině **Zobrazit** vyberte **Objekt údržby**.

    Otevře se stránka **Správa majetku** pro objekt údržby, který je přidružen k vybranému dlouhodobému majetku. (Tato stránka je obvykle k dispozici v umístění **Správa majetku \> Majetek \> Všechen majetek**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Zobrazení nákladů na údržbu přidružených k dlouhodobému majetku

Pracovní příkazy správy majetku mohou být zaúčtovány pro objekty údržby a každý z těchto pracovních příkazů obvykle obsahuje náklady. Když je dlouhodobý majetek přidružen k objektu údržby, přímo z dlouhodobého majetku můžete zobrazit související náklady.

Chcete-li zobrazit náklady na údržbu přidružené k dlouhodobému majetku, postupujte podle následujících kroků.

1. Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.
1. Vyberte majetek.
1. V podokně akcí na kartě **Správa majetku** ve skupině **Zobrazit** vyberte **Náklady na údržbu**.

    Otevře se stránka **Náklady na údržbu** a zobrazí související náklady.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Vytvoření nového objektu údržby pro existující dlouhodobý majetek

Chcete-li vytvořit nový objekt údržby pro existující dlouhodobý majetek, postupujte následovně.

1. Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.
1. Vyberte majetek.
1. V podokně akcí na kartě **Správa majetku** ve skupině **Nový** vyberte **Vytvořit objekt údržby**. (Není-li tato možnost dostupná, je možné, že objekt údržby již byl přidružen k vybranému dlouhodobému majetku.)
1. Dokončete tvorbu majetku způsobem popsaným v tématu [Vytvoření majetku](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Vytvoření nového dlouhodobého majetku a přidání nového objektu údržby pro něj

Chcete-li vytvořit nový dlouhodobý majetek a přidat pro něj nový objekt údržby, postupujte následovně.

1. Přejděte na **Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.
1. V podokně akcí zvolte **Nový**.
1. Dokončete tvorbu dlouhodobého majetku způsobem popsaným v tématu [Vytvoření dlouhodobého majetku](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. V podokně akcí na kartě **Správa majetku** ve skupině **Nový** vyberte **Vytvořit objekt údržby**.
1. Dokončete tvorbu majetku způsobem popsaným v tématu [Vytvoření majetku](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>Odebrání přidružení mezi dlouhodobým majetkem a objektem údržby

V některých případech může být nutné zrušit přidružení objektu údržby k dlouhodobému majetku. Chcete- li například [vytvořit nový objekt údržby](#new-maintenance-from-fixed) z dlouhodobého majetku, musíte nejprve odebrat existující přidružení.

Chcete-li odebrat existující přidružení mezi objektem údržby a dlouhodobým majetkem, postupujte následovně.

1. Přejděte na **Správa majetku \> Majetek \> Všechen majetek** (nebo **Aktivní majetek**).
1. Vyhledejte a otevřete dlouhodobý majetek.
1. Na záložce s náhledem **Dlouhodobý majetek** vymažte hodnotu z pole **Funkční místo**.
1. V podokně akcí vyberte **Uložit**.
