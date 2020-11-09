---
title: Pokyny, jak nastavit duální zápis
description: Toto téma popisuje scénáře, které jsou podporovány pro nastavení dvojího zápisu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088499"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>Pokyny, jak nastavit duální zápis

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Můžete nastavit připojení dvojího zápisu mezi prostředím Finance and Operations a Common Data Service.

+ **Prostředí Finance and Operations** poskytuje základní platformu pro **aplikace Finance and Operations** (například Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management a Dynamics 365 Retail).
+ **Prostředí Common Data Service** poskytuje základní platformu pro **aplikace pro zapojení zákazníků** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing a Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Modul personalistiky v aplikaci Finance and Operations podporuje připojení pro duální zápis, ale aplikace Dynamics 365 Human Resources ne.

Nastavení mechanismu se liší v závislosti na vašem předplatném a prostředí.

+ U nových instancí aplikací Finance and Operations začíná nastavení připojení dvojího zapisování v Lifecycle Services (LCS) Microsoft Dynamics. Máte-li licenci pro Power Platform, obdržíte nové prostředí Common Data Service, pokud je váš klient neobsahuje.
+ Pro existující instance aplikací Finance and Operations začíná nastavení připojení dvojího zapisování do prostředí Finance and Operations.

Než začnete s duálním zápisem na entitě, můžete spustit počáteční synchronizaci pro zpracování existujících dat na obou stranách aplikací Finance and Operations a aplikací pro zapojení zákazníků. Pokud nepotřebujete synchronizovat data mezi dvěma prostředími, můžete počáteční synchronizaci přeskočit.

Počáteční synchronizace umožňuje obousměrně kopírovat existující data z jedné aplikace do jiné. Existuje několik různých scénářů instalace v závislosti na tom, která prostředí již máte a jaký typ dat je v prostředích.

Podporovány jsou následující scénáře registrace:

+ [Nová instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků](#new-new)
+ [Nová instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků](#new-existing)
+ [Nová instance aplikace Finance and Operations, která má data, a nová instance aplikace pro zapojení zákazníků](#new-data-new)
+ [Nová instance aplikace Finance and Operations, která má data, a existující instance aplikace pro zapojení zákazníků](#new-data-existing)
+ [Existující instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků](#existing-new)
+ [Existující instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Nová instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a novou instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md). Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:

- Je zajištěno nové prázdné prostředí Finance and Operations.
- Je zřízena nová prázdná instance aplikace pro zapojení zákazníků, kde je nainstalováno základní řešení CRM.
- Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.
- Mapování entit je povoleno pro živou synchronizaci.

Obě prostředí jsou připravena k synchronizaci dat živého vysílání.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Nová instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a existující instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md). Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:

- Je zajištěno nové prázdné prostředí Finance and Operations.
- Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.
- Mapování entit je povoleno pro živou synchronizaci.

Obě prostředí jsou připravena k synchronizaci dat živého vysílání.

Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.

1. Vytvořte v aplikaci Finance and Operations novou společnost.
2. Přidejte společnost do nastavení připojení s duálním zapisováním.
3. [Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti pro Mezinárodní organizaci pro normalizaci (ISO).
4. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

Příklad a alternativní přístup viz [Příklad](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Nová instance aplikace Finance and Operations, která má data, a nová instance aplikace pro zapojení zákazníků

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má ukázková data, a novou instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu nové instance aplikace pro zapojení zákazníků](#new-new) dříve v tomto tématu. Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.

1. Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.
2. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

Příklad a alternativní přístup viz [Příklad](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Nová instance aplikace Finance and Operations, která má data, a existující instance aplikace pro zapojení zákazníků

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má data, a eistující instanci aplikace pro zapojení zákazníků, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu existující instance aplikace pro zapojení zákazníků](#new-existing) dříve v tomto tématu. Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.

1. Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.
2. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.

1. Vytvořte v aplikaci Finance and Operations novou společnost.
2. Přidejte společnost do nastavení připojení s duálním zapisováním.
3. [Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti ISO.
4. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

Příklad a alternativní přístup viz [Příklad](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Existující instance aplikace Finance and Operations a nová instance aplikace pro zapojení zákazníků

Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a novou instancí aplikace pro zapojení zákazníků probíhá v prostředí Finance and Operation.

1. [Nastavit připojení z aplikace Finance and Operations](enable-dual-write.md)
2. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

Příklad a alternativní přístup viz [Příklad](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Existující instance aplikace Finance and Operations a existující instance aplikace pro zapojení zákazníků

Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a existující instancí aplikace pro zapojení zákazníků probíhá v prostředí Finance and Operation.

1. Nastavit připojení z aplikace Finance and Operations
2. Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, [zaveďte](bootstrap-company-data.md) data Common Data Service pomocí třímístného kódu ISO společnosti.
3. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

Příklad a alternativní přístup viz [Příklad](#example).

## <a name="example"></a>Příklad

Příklad viz [Povolení Customers V3 — mapa entit kontaktů](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

Alternativní přístup založený na objemech dat v každé entitě, která potřebuje spustit počáteční synchronizaci, najdete v části [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).
