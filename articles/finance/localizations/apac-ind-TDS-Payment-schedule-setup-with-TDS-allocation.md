---
title: Nastavení platebního kalendáře s přidělením TDS
description: Toto téma vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 27f6750dd91a211ad12a1bd5d9c4ab9a2e1e4a79
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358403"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Nastavení platebního kalendáře s přidělením TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit plány plateb s alokací daně odečtené u zdroje (TDS).

1. Přejděte do nabídky **Závazky \> Nastavení platby \> Platební kalendáře**.

    [![Stránka Platební kalendáře.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. V podokně akcí vyberte **Nový** pro vytvoření platebního kalendáře a zadejte požadované údaje.
3. V poli **Přidělení** vyberte metodu, která se použije k alokaci platby pro časový plán plateb:

    - Celkem
    - Pevná částka
    - Fixní množství
    - Určeno

    Pole **Přidělení srážkové daně** zobrazuje metodu přidělení TDS pro plán plateb. Pokud vyberete **Součet** v poli **Přidělení**, pole **Přidělení srážkové daně** je automaticky nastaveno na **Součet**. Pokud vyberete **Pevná částka**, **Pevné množství** nebo **Specifikováno** v poli **Přidělení**, pole **Přidělení srážkové daně** je automaticky nastaveno na **Proporčně**.

    > [!NOTE]
    > Pokud je pole **Přidělení srážkové daně** nastaveno na **Součet**, splátky plateb se počítají na základě hrubé částky, která zahrnuje částku TDS. Pokud je pole **Přidělení srážkové daně** nastaveno na **Proporčně**, splátky plateb se počítají na základě čisté částky faktury po odečtení částky TDS.

4. Zadejte další požadované údaje a poté zavřete stránku.
