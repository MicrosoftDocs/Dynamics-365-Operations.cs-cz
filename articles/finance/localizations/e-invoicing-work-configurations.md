---
title: Práce s konfiguracemi
description: Tento článek poskytuje přehled hlavního scénáře pro práci s konfiguracemi elektronického hlášení (ER) z pracovního prostoru Funkce globalizace.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: d87559405d2490c314eb2c8b88268af0dc0dfaca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283048"
---
# <a name="work-with-configurations"></a>Práce s konfiguracemi

[!include [banner](../includes/banner.md)]

Konfigurace elektronického výkaznictví (ER) jsou jednou z hlavních sad komponent funkcí elektronické fakturace. Konfigurace ER obsahuje nastavení struktury souboru a sadu transformačních pravidel pro transformaci dat dvěma způsoby:

- **Export konfigurace formátu ER** – Tato konfigurace převádí data z jednotné vnitřní struktury (model ER) do formátu elektronického souboru.
- **Import konfigurace formátu ER** – Tato konfigurace převádí data z formátu elektronického souboru do jednotné vnitřní struktury (model ER).

Kromě generování odchozích elektronických souborů v předdefinovaném formátu se konfigurace ER široce používají k analýze příchozích zpráv z externích webových služeb jako odpovědí. Tato funkce pomáhá budovat konfigurovatelnou logiku pro získání výsledků komunikace s externími kanály, převedení těchto výsledků (kódy, zprávy a protokoly) do uživatelsky čitelné struktury a poté předání těchto informací klientské aplikaci.

Chcete-li začít používat konfigurace ER ve své funkci elektronické fakturace, musíte je propojit s funkcí a zpřístupnit je na kartě **Konfigurace** pro aktuální verzi funkce. S propojenou konfigurací ER můžete pracovat výběrem možnosti **Přidat**, **Odstranit**, **Upravit**, nebo **Zobrazit**.

Než budete moci přidat odkaz na konfiguraci ER, konfigurace musí existovat ve vašem úložišti Regulatory Configuration Service (RCS). Chcete-li zkontrolovat konfigurace ER, které jsou k dispozici ve vašem úložišti RCS, postupujte takto.

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Elektronické výkaznictví** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.

Informace o tom, jak vytvořit novou konfiguraci ER nebo importovat existující konfiguraci ER z globálního úložiště, viz [Elektronické vykazování](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Chcete-li upravit konfiguraci připojeného ER, vyberte **Upravit** na kartě **Konfigurace** pro aktuální funkci elektronické fakturace. Systém automaticky vytvoří verzi konfigurace ER. Pokud aktuální verzi nevytvořil aktivní poskytovatel konfigurace, systém vytvoří odvozenou verzi, která používá vašeho poskytovatele konfigurace. Pokud byla aktuální verze vytvořena aktivním poskytovatelem konfigurace, systém vytvoří novou verzi. V obou případech můžete upravit vytvořenou verzi a poté automaticky provést všechny požadované aktualizace.
