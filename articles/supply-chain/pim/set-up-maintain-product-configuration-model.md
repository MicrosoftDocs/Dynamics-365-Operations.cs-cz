---
title: Nastavení modelu konfigurace produktu
description: Tento článek popisuje postup nastavení a vytvoření modelu konfigurace produktu.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7af9aaa01d89da909f2b30089c17d67d377d9e78
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423915"
---
# <a name="set-up-a-product-configuration-model"></a>Nastavení modelu konfigurace produktu

[!include [banner](../includes/banner.md)]

Tento článek popisuje postup nastavení a vytvoření modelu konfigurace produktu.

| Úkol                                                        | popis                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vytvoření základního produktu.                                    | Vytvořte hlavní produkt ze seznamu **Základní produkt**. Uvolněte základní produkt do všech příslušných společností. Pro základní produkt používaný jako verzi pro model konfigurace produktu nebo dílčí komponentu je nutné vybrat **Konfigurace založená na omezeních** jako technologii konfigurace, a konfigurační dimenze musí být vybrány pouze pro skupinu dimenzí produktu. |
| Tvorba komponent.                                          | Vytvořte součásti na stránce **Komponenty**. Komponenty jsou stavební kameny modelu konfigurace produktu a lze je znovu použít ve více modelech konfigurace produktu.                                                                                                                                                                                                                      |
| Tvorba typů atributů.                                     | Vytvořte typy atributů na stránce **Typy atributů**. Typy atributu určují sadu datových typů všech atributů, které jsou použity v modelech konfigurace výrobku. Atributy **Logická**, **Text** s pevným seznamem a **Celé číslo** s rozsahem typů tvoří seznam hodnot, které jsou k dispozici, když konfigurujete variantu produktu založenou na modelu konfigurace produktu.       |
| Vytvoření nového modelu konfigurace produktu.                       | Vytvořte model konfigurace produktu na stránce **Nový model konfigurace produktu**.                                                                                                                                                                                                                                                                                                              |
| Přidání atributů do modelu konfigurace produktu.            | Vytvořte atribut na pevné kartě **Atributy** na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních**. Atributy popisují funkce modelu konfigurace produktu.                                                                                                                                                                                                       |
| Přidání omezení do modelu konfigurace produktu.           | Vytvořte omezení na pevné kartě **Omezení** na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních**. Omezení jsou omezení, která musí splnit konfigurace produktu. Omezení může být omezení výrazů nebo omezení tabulek.                                                                                                                                 |
| Přidání dílčích součástí do modelu konfigurace produktu.         | Vytvořte dílčí součásti na pevné kartě **Dílčí součásti** na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních**. Dílčí součásti souvisí s komponentami a jsou propojeny s položkami reprezentujícími dílčí komponentu.                                                                                                                                                                       |
| Přidání uživatelských požadavků do modelu konfigurace produktu.     | Požadavky uživatelů jsou podobné dílčím součástem, ale neodkazují na položky. Můžete považovat uživatelské požadavky za fiktivní kusovník. Všechny řádky kusovníku nebo operace postupu, které jsou umístěny přímo pod požadavek uživatele, budou sbalené do nadřízené součásti.                                                                                                                       |
| Přidání řádků kusovníku do modelu konfigurace produktu.             | Vytvořte řádky kusovníku na pevné kartě **Řádky kusovníku** na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních**. Řádky kusovníku představují součást, která je třeba pro vytvoření varianty produktu.                                                                                                                                                                                                 |
| Přidání operací postupu do modelu konfigurace produktu.      | Vytvořte operace postupu na pevné kartě **Operace postupu** na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních**. Operace postupu představují krok v sérii kroků, které se provádějí pro vytvoření varianty produktu.                                                                                                                                                    |
| Vytvoření aktivní verze pro model konfigurace produktu. | Vytvořte aktivní verzi modelu konfigurace produktů na stránce **Verze**. Verze je vztah mezi modelem konfigurace produktu a základním produktem. Model konfigurace produktu, který má aktivní verzi, lze konfigurovat z prodejní objednávky, prodejní nabídky, nákupní objednávky nebo výrobní zakázky.                                                               |
| Testování modelu konfigurace produktu.                         | Testujte model konfigurace produktu ze stránky **Podrobnosti modelu produktu s konfigurací založenou na omezeních** nebo **Seznam modelů konfigurace produktu**. Testování modelů konfigurace produktu simuluje proces konfigurace modelu výrobku, ke kterému dochází během zpracování objednávky.                                                                                                |
| Vytvoření šablony modelů konfigurace produktu.                | Vytvořte šablonu modelu konfigurace produktu na stránce **Šablony konfigurací**. Konfigurační šablona obsahuje hodnoty pro atributy v modelu konfigurace produktu. Vyberte hodnoty atributu na stránce **Řádek konfigurace**. Můžete se rozhodnout načíst šablonu konfigurace modelu výrobku při konfiguraci modelu výrobku.                                                   |
| Konfigurace položky.                                          | Modely konfigurace produktu lze konfigurovat z prodejní objednávky, prodejní nabídky, nákupní objednávky nebo výrobní zakázky.                                                                                                                                                                                                                                                                           |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]