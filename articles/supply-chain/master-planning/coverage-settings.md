---
title: Nastavení distponibility
description: Toto téma poskytuje informace o nastavení disponibility, které hlavní plánování používá k výpočtu požadavků na položky.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaacf28701542d329afedd8206a12f7c11b7ac7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999974"
---
# <a name="coverage-settings"></a>Nastavení distponibility

[!include [banner](../includes/banner.md)]

Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku.

Existuje několik způsobů, jak zadat nastavení disponibility:

- Nastavte disponibilitu skupiny.

    Můžete vytvořit skupinu disponibility, která obsahuje nastavení pro všechny produkty spojené s touto skupinou disponibility. Přejděte na **Hlavní plánování &gt; Nastavení &gt; Disponibilita &gt; Skupiny disponibility** a vytvořte tak skupinu disponibility. Můžete propojit skupinu disponibility s produktem. Pokud je odkaz na konkrétní pracoviště, sklad nebo dimenze produktu, použijte pole **Skupina disponibility** na stránce **Disponibilita položky**. Pokud je propojení obecné, bez ohledu na dimenze produktu, použijte pole **Skupina disponibility** na pevné záložce **Plán** stránky **Podrobnosti o produktu**. Pokud ve výchozím nastavení nespojíte skupinu disponibility s produktem, hlavní plánování bude používat obecnou skupinu disponibility, která je určena na stránce **Parametry hlavního plánování**.

- Nastavte disponibilitu produktu.

    Nastavení pokrytí lze vytvořit pro určitý produkt. Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**. Vyberte produkt a pak v podokně akcí na kartě **Plán** ve **skupině disponibility** zvolte **Disponibilita položky** pro otevření stránky **Disponibilita položky**. Je-li produkt již spojen se skupinou disponibility, můžete nastavení skupiny disponibility přepsat v poli **Přepsat**. Nastavení disponibility na stránce **Disponibilita položky** má přednost před nastavením na stránce **Skupina disponibility**.

- Nastavení disponibility produktu pomocí průvodce.

    Průvodce vás provede jednotlivými kroky procesu nastavení parametrů disponibility primární položky. Na stránce **Disponibilita položky** v podokně akcí zvolte **Průvodce** a otevřete **Průvodce disponibilitou položky**.

- Nastavení disponibility pro skupinu dimenzí.

    Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**. Na stránce **Podrobnosti o uvolněném produktu** na záložce s náhledem **Obecné** v části **Správa** zvolte odkaz v poli **Skupina dimenze úložiště**. Na stránce **Skupiny dimenze úložiště** vyberte zaškrtávací pole **Plán disponibility podle dimenzí** a vytvořte tak nastavení disponibility pro dimenzi ve skupině dimenzí úložiště. Pole **Plán disponibility podle dimenzí** musí mít vybráno pro všechny dimenze produktu, jako je například konfigurace, barva, velikost nebo styl.


## <a name="coverage-codes"></a>Kódy pokrytí

Hlavní plánování lze nakonfigurovat tak, aby používalo různé metody doplnění. Metody doplnění nebo metody určení velikosti šarží jsou techniky používanými systémem ke stanovení velikosti dávky pro nakoupené nebo vyráběné položky. 

Každá metoda doplnění je přiřazena k jednomu z následujících kódů pokrytí:

- **Ruční** - určení velikosti šarže, při kterém systém nenavrhuje nákup, převod nebo výrobní objednávky pro danou položku. Plánovač pro danou položku bude mít na starosti vytváření požadovaných objednávek pro doplnění položky.
- **Podle požadavku** – velikost šarže, při které systém vytváří plánovaný nákup, převod nebo výrobní zakázku podle požadavků na položku. Obvykle se používá pro nákladné položky s nárazovou poptávkou.  
- **Za období** - určení velikosti šarže, které kombinuje všechny požadavky na období do jedné objednávky pro danou položku. Zakázka bude naplánována pro první den období a její množství bude plnit čisté požadavky během stanoveného období. Toto období začíná první poptávkou položky a pokrývá určenou délku v čase. Další období bude začínat následujícími požadavky položky.
- **Min/max** – metoda velikosti šarže, která obsahuje doplnění zásob na určitou úroveň, pokud je odhadovaná zásoba nižší než prahová hodnota. Množství doplnění bude rozdíl mezi maximální úrovní a předpokládanou úrovní zásob na skladě.


## <a name="additional-resources"></a>Další zdroje

[Přehled hlavních plánů](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]