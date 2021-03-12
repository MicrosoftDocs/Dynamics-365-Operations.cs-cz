---
title: Zahrnutí hmotnosti kontejneru a objemu při naložení
description: Toto téma popisuje, jak nastavit a použít funkci zahrnutí hmotnosti kontejneru a objemu v nákladech.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8fb40a0fe1606b856f58f5bc517c7f1aff85e4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977506"
---
# <a name="include-container-weight-and-volume-on-load"></a>Zahrnutí hmotnosti kontejneru a objemu při naložení

[!include [banner](../includes/banner.md)]

Funkce pro zahrnutí hmotnosti kontejneru a objemu v nákladu poskytuje jasnou představu celkové hmotnosti a objemu kontejnerů a zboží, které bude součástí nákladu.

Náklad obsahuje jednu nebo více dodávek a tyto dodávky obsahují různé položky, které patří do jedné nebo více prodejních objednávek. Položky jsou uloženy uvnitř kontejneru a kontejnery jsou naloženy na náklad. Položky mimo kontejner mohou být též součástí nákladu. Na základě těchto podmínek systém vypočítá hodnoty hmotnosti a objemu v nákladu podle hmotnosti a objemu obou kontejnerů a zboží.

Nejsou-li vypočtené hodnoty přesné, lze je upravit zadáním skutečných hodnot hmotnosti a objemu v nákladu. Hodnoty hmotnosti a objemu se používají v procesech správy přepravy. Například hodnoty se používají v pracovní ploše sazby trasy, kde pomáhají definovat sazbu a trasu pro náklad, a také se používají pro úhrady za přepravu a přihlášení řidiče.

## <a name="where-it-applies"></a>Kdy se to používá

Funkce pro zahrnutí objemu a hmotnosti kontejneru do nákladu se použije v procesech správy přepravy, jako je například pracovní plocha sazeb trasy, úhrady za přepravu nebo přihlášení řidiče.

## <a name="how-it-is-set-up"></a>Způsob nastavení

Počet kontejnerů, které je potřeba zvážit pro náklad, je vypočítán za základě hmotnosti a objemu kontejneru, a na použitém procentu kontejneru.

-   Chcete-li nastavit hmotnost a objem kontejneru, klikněte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Typy kontejnerů**.

-   Chcete-li nastavit procento využití kontejneru, klikněte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Skupiny kontejnerů** a zadejte hodnotu do pole **Procento využití kontejneru**.
