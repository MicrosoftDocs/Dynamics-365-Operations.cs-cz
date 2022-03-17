---
title: Práce s konfiguracemi
description: Toto téma poskytuje přehled hlavního scénáře pro práci s konfiguracemi elektronického hlášení (ER) z pracovního prostoru Funkce globalizace.
author: dkalyuzh
ms.date: 01/26/2022
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
ms.openlocfilehash: 4318399ee58ed54b29f8d360345b8930238ea9f2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371586"
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
