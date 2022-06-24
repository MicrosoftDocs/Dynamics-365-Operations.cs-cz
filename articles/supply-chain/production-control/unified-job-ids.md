---
title: Sjednocená číselná řady pro ID úloh
description: Tato funkce poskytuje jednu jednotnou číselnou řadu, která generuje ID úloh pro moduly řízení výroby, provádění výroby a modul času a docházky.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 301a4bb58f896a2dc0f0cddcd2e29344865ca898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897538"
---
# <a name="unified-number-sequence-for-job-ids"></a>Sjednocená číselná řady pro ID úloh

[!include [banner](../includes/banner.md)]

Tato funkce poskytuje jednu jednotnou číselnou řadu, která generuje ID úloh pro moduly řízení výroby, provádění výroby a modul času a docházky. Dříve jste pro každý z těchto modulů mohli zvolit jinou číselnou řadu, což mohlo vést ke konfliktním ID úloh, pokud dvě nebo více těchto řad používaly stejný formát. Takový konflikt může způsobit poškození dat.

## <a name="turn-on-this-feature-for-your-system"></a>Zapnutí této funkce ve vašem systému

Pokud váš systém ještě neobsahuje funkci popsanou v tomto článku, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Sjednocená číselná řada pro ID úloh*.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Nastavení sjednocené číselné řady pro ID úloh

Po povolení této funkce budou nastavení číselné řady **Identifikace úlohy**, která se nachází na stránkách parametrů pro moduly Řízení výroby, Provádění výroby a Čas a docházka, zastaralá a bude přidáno nové pole **Sjednocené ID úlohy**. Hodnota **Sjednocené ID úlohy** je sdílena všemi třemi moduly, čímž je zajištěno, že všechny moduly odkazují na stejnou číselnou řadu. ID úloh proto budou ve všech třech modulech jedinečná a ke konfliktu nikdy nedojde.

Nastavení sjednocené číselné řady pro ID úloh:

1. Zapněte funkci, jak je popsáno v předchozí části.
1. Buď identifikujte číselnou řadu, kterou chcete použít pro vaše sjednocená ID úlohy, nebo vytvořte novou. Další informace naleznete v tématu [Přehled číselných řad](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Přejděte na stránku **Parametry řízení výroby**, **Parametry provedení výroby** nebo **Parametry času a docházky**. Nezáleží na tom, kterou z nich si vyberete, protože když toto nastavení provedete na kterékoli z těchto stránek, všechny ostatní stránky se automaticky aktualizují.
1. Otevřete kartu **Číselné řady** na stránce s vybranými parametry.
1. Přiřaďte **Kód číselné řady**, který jste dříve identifikovali, k řádku **Sjednocená ID úloh** v mřížce.
