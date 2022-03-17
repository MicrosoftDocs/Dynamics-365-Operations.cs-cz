---
title: Nastavení Regulatory Configuration Service (RCS)
description: Toto téma vysvětluje, jak nastavit Regulatory Configuration Service (RCS).
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 33aab6f0a482ce3d90a7e9828015a8e7bebb7827
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371591"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Nastavení Regulatory Configuration Service (RCS)

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit Regulatory Configuration Service (RCS).

## <a name="turn-on-globalization-features"></a>Zapnutí funkcí globalizace

1. Přihlaste se k účtu RCS.
2. Vyberte dlaždici **Správa funkcí**.
3. V pracovním prostoru **Správa funkcí** vyberte pracovní prostor **Funkce globalizace** v seznamu a poté vyberte **Povolit hned**.

Dlaždice pro pracovní prostor **Funkce globalizace** by se nyní měla objevit na hlavním řídicím panelu RCS.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Nastavení parametrů pro integraci RCS s Elektronickou fakturací

1. V pracovním prostoru **Funkce globalizace** v části **Související nastavení** vyberte **Parametry elektronického výkaznictví**.
2. Na kartě **Elektronická fakturace** v poli **Identifikátor URI koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Microsoft Azure, jak je znázorněno v následující tabulce.

    | Geografie datového centra Azure | URI adresa koncového bodu služby |
    |----------------------------|----------------------|
    | Spojené státy              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Evropa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Spojené království             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asie                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japonsko                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Ověřte, zda je pole **ID aplikace** nastaveno na **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Tato hodnota je pevná hodnota. Ujistěte se, že je zadán pouze globálně jedinečný identifikátor (GUID) a že hodnota neobsahuje žádné další symboly, jako jsou mezery, čárky, tečky nebo uvozovky.
4. V poli **ID prostředí LCS** zadejte ID prostředí Microsoft Dynamics Lifecycle Services LCS. Tato hodnota je odkazem na prostředí Finance nebo Supply Chain Management, které budete používat se službou Elektronická fakturace. Chcete-li získat své ID, přihlaste se k [LCS](https://lcs.dynamics.com/), otevřete svůj projekt a poté na kartě **Spravovat prostředí** v části **Údaje o prostředí** vyhledejte pole **ID prostředí**.

    > [!IMPORTANT]
    > Pokud je nainstalován doplněk elektronické fakturace ve více prostředích Finance nebo Supply Chain Management v LCS, vždy použijte ID prostředí naposledy nainstalovaného prostředí. Pokud se rozhodnete nainstalovat doplněk v novém prostředí po nastavení a práci s funkcí elektronické fakturace, aktualizujte pole **ID prostředí LCS** v RCS na nejnovější hodnotu.

5. Zvolte **Uložit** a pak zavřete stránku.

## <a name="configuration-providers"></a>Poskytovatelé konfigurace

Pomocí poskytovatelů konfigurace můžete rozlišit vlastníky konfigurací elektronického výkaznictví (ER), které se používají v procesech elektronické fakturace, a vlastníky funkcí globalizace. U všech funkcí globalizace, které poskytuje společnost Microsoft a jsou publikovány v globálním úložišti, je poskytovatel konfigurace nastaven na **Microsoft** (`http://microsoft.com`).

Můžete upravit pouze konfigurace ER a funkce globalizace, které patří aktivnímu poskytovateli konfigurace. Tyto konfigurace a funkce můžete použít jako šablony k vytvoření konfigurací a funkcí, které patří aktivnímu poskytovateli konfigurace, abyste je mohli upravit.

Nejprve vytvořte poskytovatele konfigurace. Poté jednoho z nich nastavte jako aktivního. Nemůžete nastavit poskytovatele konfigurace **Microsoft** jako aktivního.

### <a name="create-a-configuration-provider"></a>Vytvoření poskytovatele konfigurace

1. V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Poskytovatelé konfigurace**.
2. Zvolte **Nové**.
3. V poli **Název** zadejte jedinečný název poskytovatele konfigurace.
4. V poli **Internetová adresa** zadejte jedinečnou adresu URL poskytovatele konfigurace.
5. Zvolte **Uložit** a pak zavřete stránku.

### <a name="select-a-configuration-provider-as-active"></a>Výběr poskytovatele konfigurace jako aktivního

1. V seznamu poskytovatelů konfigurace vyberte poskytovatele konfigurace, kterého chcete nastavit jako aktivního.
2. Vyberte **Nastavit jako aktivní**.

## <a name="import-er-configurations-from-the-global-repository"></a>Import konfigurací elektronického výkaznictví z globálního úložiště

1. V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Poskytovatelé konfigurace**.
2. V seznamu poskytovatelů konfigurace vyberte **Microsoft** a poté vyberte **Úložiště**.
3. Vyberte **Globální** a v podokně akcí vyberte **Otevřít**.
4. Importujte následující modely ER:

    - **Model kontextu faktury odběratele**
    - **Model faktury**
    - **Fiskální dokumenty** (pro brazilské scénáře, je-li to požadováno)
    - **Model zprávy odpovědi**

5. Pokud **Mapování modelu faktury** nebylo automaticky importováno, importujte ho.
6. Zavřete stránku.
