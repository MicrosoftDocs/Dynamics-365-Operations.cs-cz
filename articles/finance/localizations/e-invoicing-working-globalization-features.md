---
title: Komponenty funkce globalizace
description: Tento článek poskytuje přehled komponent funkce globalizace.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5525332fe3f1a3ea96da630dc34bab82e4117f99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891481"
---
# <a name="globalization-feature-components"></a>Komponenty funkce globalizace

[!include [banner](../includes/banner.md)]

Funkce globalizace je sada komponent, které definují pravidla pro transformaci dat v konfiguracích elektronického hlášení (ER). Tyto komponenty zahrnují instrukce pro zpracování elektronických dokumentů a jejich následné odeslání nebo příjem z externích kanálů. Zahrnují také podmínky, které definují, kdy má být funkce spuštěna pro příchozí obchodní data.

Všechny komponenty na sobě závisí. Funkce globalizace usnadňují vytváření a udržování této závislosti a podporují správu životního cyklu a verzování sady komponent.

## <a name="access-electronic-invoicing-feature-components"></a>Přístup ke komponentům funkcí elektronické fakturace 

1. Přihlaste se ke svému účtu Regulatory Configuration Service (RCS).
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.

    Funkce globalizace mají několik součástí. Stránka **Funkce elektronické fakturace** obsahuje samostatnou kartu pro každou komponentu.

    - **Verze** – Tato součást podporuje správu životního cyklu funkce. Můžete jej použít ke správě stavu pro různé verze funkce.
    - **Konfigurace** – Tato komponenta umožňuje spravovat, prohlížet a upravovat související konfigurace formátu ER a mapování formátu, které se používají v procesu zpracování.
    - **Nastavení** - Tato součást umožňuje uživatelům globalizačních služeb, jako je například elektronická fakturace, spravovat nastavení související verze funkce. Proto podporuje flexibilní sestavování pravidel komunikace a odpovědí.
    - **Prostředí** - Tato součást umožňuje uživatelům globalizačních služeb, jako je například elektronická fakturace, spravovat prostředí, ve kterém se používá nastavení verze funkce. Umožňuje jim také udělit oprávnění uživatelům, kteří budou mít přístup k nastavení verze funkce.
    - **Organizace** - Tato součást umožňuje uživatelům sdílet tuto funkci s externími organizacemi.
    - **Tagy** – Tato komponenta umožňuje označit funkce, které lze použít v plánu globalizace jako referenci.
