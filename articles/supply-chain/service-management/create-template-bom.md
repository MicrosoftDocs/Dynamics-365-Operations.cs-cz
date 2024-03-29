---
title: Vytvoření šablony kusovníku
description: Šablonu kusovníku lze vytvořit pomocí mnoha metod.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 169b54a0509a2e11ce2e888404da10fd81db475e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678199"
---
# <a name="create-a-template-bom"></a>Vytvoření šablony kusovníku   

[!include [banner](../includes/banner.md)]


Šablonu kusovníku lze vytvořit pomocí kterékoli z následujících metod. U všech těchto metod jsou pole **Od data** a **Do data** nepovinná a slouží pouze pro informaci.

## <a name="create-a-template-bom-manually"></a>Ruční vytvoření šablony kusovníku

1.  Přejděte na **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.

2.  Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.

3.  Ve skupinovém rámečku **Kopírovat řádky kusovníku z odkazu** vyberte možnost **ruční**.

4.  Do pole **Číslo položky** zadejte položku typu **Kusovník**.

5.  Do pole **Název** zadejte název šablony.

6.  Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.

7.  Vyberte **OK**.

Je vytvořena nová prázdná šablona kusovníku.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Vytvoření šablony kusovníku na základě jiné šablony kusovníku

1.  Vyberte **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.

2.  Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.

3.  Ve skupinovém rámečku **Kopírovat řádky kusovníku z odkazu** vyberte možnost **Šablona kusovníku**.

4.  V poli **Referenční číslo** vyberte stávající šablonu kusovníku, kterou chcete zkopírovat do nové šablony kusovníku.

5.  Do pole **Název** zadejte název šablony.

6.  Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.

7.  Vyberte **OK**.

Je vytvořena nová šablona kusovníku pomocí řádků odpovídajících řádkům původní šablony kusovníku.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Vytvoření šablony kusovníku na základě kusovníku položky

1.  Vyberte **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.

2.  Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.

3.  Ve skupinovém rámečku **Kopírování řádků kusovníku z odkazu** vyberte **Kusovník**.

4.  V poli **referenční číslo** vyberte verzi Kusovníku. Položka typu kusovníku je zkopírována do **číslo položky**.

5.  Do pole **Název** zadejte název šablony.

6.  Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.

7.  Vyberte **OK**.

Je vytvořena nová šablona kusovníku s využitím řádků odpovídajících řádkům kusovníku uvedeného v poli **Kusovník**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Vytvoření šablony kusovníku na základě kusovníku výroby

1.  Vyberte **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.

2.  Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.

3.  Ve skupinovém rámečku **Kopírování řádků kusovníku z odkazu** vyberte **Výroba**.

4.  V poli **referenční číslo** vyberte kusovník výroby.

5.  Do pole **Název** zadejte název šablony.

6.  Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.

7.  Vyberte **OK**.

Je vytvořena nová šablona kusovníku s využitím řádků odpovídajících řádkům kusovníku uvedeného v poli **BOM**.

## <a name="see-also"></a>Viz také

[Kusovníky šablony](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]