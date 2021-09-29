---
title: Přidání datových polí do daňových konfigurací
description: Toto téma vysvětluje, jak přizpůsobit daňové konfigurace přidáním datových polí.
author: Kai-Cloud
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fb10fb5feb317dca5253eea6e5694a3960a58a7d
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500137"
---
# <a name="add-data-fields-in-tax-configurations"></a>Přidání datových polí do daňových konfigurací

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak přizpůsobit daňové konfigurace pomocí [datových polí, která jsou přidána do daňové integrace](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Přizpůsobení datového modelu daně

1. V Microsoft Dynamics 365 Finance přejděte do **Elektronické výkaznictví** > **Konfigurace daní**.
2. Ve stromu konfigurace vyberte položku **Daňový datový model - Evropa**. Poté v podokně akcí vyberte příkaz **Vytvořit konfiguraci**.
3. V rozevíracím dialogovém okně vyberte **Model zdanitelného dokladu odvozený z názvu: Daňový datový model – Evropa, Microsoft**, zadejte název nového daňového datového modelu a poté vyberte příkaz **Vytvořit konfiguraci**.
4. Vyberte daňový datový model, který jste právě vytvořili, a poté v podokně akcí vyberte **Návrhář**.
5. Rozbalte strom datového modelu, vyberte **Řádky** a potom vyberte příkaz **Nový**.
6. V dialogovém okně **Vytvořit uzel** zadejte název, zadejte typ položky a poté vyberte **Přidat**.
7. Přidejte všechny povinné sloupce.
8. V podokně akcí vyberte příkaz **Uložit** a potom vyberte možnost **Dokončit**.
9. Zavřete stránku a zobrazte dokončenou verzi daňového datového modelu.

## <a name="customize-the-tax-configuration"></a>Přizpůsobení konfigurace daně

1. Ve Finance přejděte do nabídky **Elektronické výkaznictví** > **Konfigurace daní**.
2. Ve stromu konfigurace vyberte položku **Konfigurace daně – Evropa**. Poté v podokně akcí vyberte příkaz **Vytvořit konfiguraci**.
3. V rozevíracím dialogovém okně vyberte **Konfiguraci daňové služby odvozená z názvu: Konfigurace dně – Evropa, Microsoft**, zadejte název nové daňové konfigurace a poté vyberte příkaz **Vytvořit konfiguraci**.
4. Vyberte konfiguraci daně, kterou jste právě vytvořili, a poté v podokně akcí vyberte **Návrhář**.
5. V části **Vlastnosti** v poli **Datový model** vyberte přizpůsobený daňový datový model, který jste vytvořili dříve.
6. V poli **Verze datového modelu** vyberte dokončenou verzi daňového datového modelu.
7. Vyberte příkaz **Přidat** a přidejte požadovaná daňová opatření.
8. V podokně akcí vyberte příkaz **Uložit** a potom vyberte možnost **Dokončit**.
9. Zavřete stránku a zobrazte dokončenou verzi daňové konfigurace.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Implementujte daňové funkce v přizpůsobené daňové konfiguraci

1. Ve službě Regulatory Configuration Service (RCS) přejděte do nabídky **Funkce globalizace** > **Daň**.
2. Vyberte příkaz **Přidat**, zadejte informace o nové funkci a poté vyberte **Vytvořit funkci**.
3. Na kartě **Verze** vyberte funkci a poté vyberte příkaz **Upravit**.
4. Na kartě **Obecné** v poli **Verze konfigurace** vyberte přizpůsobenou konfiguraci a verzi daně.
5. V dialogovém okně **Spravovat sloupce** vyberte sloupce záhlaví a řádků, které chcete zahrnout do přizpůsobeného daňového opatření, a poté je kliknutím na tlačítko se šipkou doprava přidejte do seznamu **Vybrané sloupce**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
