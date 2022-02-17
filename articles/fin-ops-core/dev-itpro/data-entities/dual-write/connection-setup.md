---
title: Pokyny pro nastavení duálního zápisu
description: Toto téma popisuje scénáře, které jsou podporovány pro nastavení dvojího zápisu.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6de449b14bcdd82336e3e255bf62ad069d3daaf5
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061597"
---
# <a name="guidance-for-dual-write-setup"></a>Pokyny pro nastavení duálního zápisu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Můžete nastavit připojení dvojího zápisu mezi prostředím Finance a Operace a Dataverse.

+ Prostředí **Finance a Operace** poskytuje základní platformu pro **finanční a provozní aplikace** (například Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce a Dynamics 365 Human Resources).
+ Prostředí **Dataverse** poskytuje základní platformu pro **aplikace Customer Engagement** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing a Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Modul personalistiky v aplikaci Dynamics 365 Finance podporuje připojení pro duální zápis, ale aplikace Dynamics 365 Human Resources ne.

Nastavení mechanismu se liší v závislosti na vašem předplatném a prostředí:

+ U nových instancí finančních a provozních aplikací začíná nastavení připojení dvojího zapisování v Microsoft Dynamics Lifecycle Services (LCS). Máte-li licenci pro Microsoft Power Platform, obdržíte nové prostředí Dataverse, pokud je váš klient neobsahuje.
+ U stávajících instancí finančních a provozních aplikací začíná nastavení připojení dvojího zapisování v prostředí Finance a Operace.

Než začnete s duálním zápisem na entitě, můžete spustit počáteční synchronizaci pro zpracování existujících dat na obou stranách: u finančních a provozních aplikací a aplikací Customer Engagement. Pokud nepotřebujete synchronizovat data mezi dvěma prostředími, můžete počáteční synchronizaci přeskočit.

Počáteční synchronizace umožňuje obousměrně kopírovat existující data z jedné aplikace do jiné. Existuje několik scénářů instalace v závislosti na tom, která prostředí již máte a jaký typ dat se v nich nachází.

Podporovány jsou následující scénáře registrace:

+ [Nová instance finanční a provozní aplikace a nová instance aplikace Customer Engagement](#new-new)
+ [Nová instance finanční a provozní aplikace a stávající instance aplikace Customer Engagement](#new-existing)
+ [Nová instance finanční a provozní aplikace, která má data, a nová instance aplikace Customer Engagement](#new-data-new)
+ [Nová instance finanční a provozní aplikace, která má data, a stávající instance aplikace Customer Engagement](#new-data-existing)
+ [Stávající instance finanční a provozní aplikace a nová instance aplikace Customer Engagement](#existing-new)
+ [Stávající instance finanční a provozní aplikace a stávající instance aplikace Customer Engagement](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Nová instance finanční a provozní aplikace a nová instance aplikace Customer Engagement

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí finanční a provozní aplikace, která neobsahuje žádná data a novou instanci aplikace Customer Engagement, postupujte podle kroků v nastavení [dvojího zápisu z Lifecycle Services](lcs-setup.md). Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:

- Je zřízeno nové prázdné prostředí Finance a Operace.
- Je zřízena nová prázdná instance aplikace pro zapojení zákazníků, kde je nainstalováno základní řešení CRM.
- Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.
- Mapování tabulek je povoleno u živé synchronizace.

Obě prostředí jsou připravena k synchronizaci dat živého vysílání.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Nová instance finanční a provozní aplikace a stávající instance aplikace Customer Engagement

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí finanční a provozní aplikace, která neobsahuje žádná data a stávající instanci aplikace Customer Engagement, postupujte podle kroků v nastavení [dvojího zápisu z Lifecycle Services](lcs-setup.md). Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:

- Je zřízeno nové prázdné prostředí Finance a Operace.
- Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.
- Mapování tabulek je povoleno u živé synchronizace.

Obě prostředí jsou připravena k synchronizaci dat živého vysílání.

Chcete-li synchronizovat existující data Dataverse s finanční a provozní aplikací, postupujte podle následujících kroků.

1. Vytvoření nové společnosti ve finanční a provozní aplikaci.
2. Přidejte společnost do nastavení připojení s duálním zapisováním.
3. [Zavedení](bootstrap-company-data.md) dat Dataverse pomocí třímístného kódu společnosti pro Mezinárodní organizaci pro normalizaci (ISO).
4. Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.

Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example) dále v tomto tématu.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Nová instance finanční a provozní aplikace, která má data, a nová instance aplikace Customer Engagement

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí finanční a provozní aplikace, která má ukázková data, a novou instanci aplikace Customer Engagement, postupujte podle kroků v části [Nová instance finanční a provozní aplikace a nová instance aplikace Customer Engagement](#new-new) výše v tomto tématu. Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.

1. Otevřete finanční a provozní aplikaci ze stránky LCS, přihlaste se a pak přejděte ke **Správa dat \> Dvojí zápis**.
2. Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.

Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Nová instance finanční a provozní aplikace, která má data, a stávající instance aplikace Customer Engagement

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí finanční a provozní aplikace, která má ukázková data, a stávající instanci aplikace Customer Engagement, postupujte podle kroků v části [Nová instance finanční a provozní aplikace a stávající instance aplikace Customer Engagement](#new-existing) výše v tomto tématu. Chcete-li v aplikaci synchronizovat data s aplikací pro zapojení zákazníků, postupujte po dokončení nastavení připojení následujícím způsobem.

1. Otevřete finanční a provozní aplikaci ze stránky LCS, přihlaste se a pak přejděte ke **Správa dat \> Dvojí zápis**.
2. Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.

Chcete-li synchronizovat existující data Dataverse s finanční a provozní aplikací, postupujte podle následujících kroků.

1. Vytvoření nové společnosti ve finanční a provozní aplikaci.
2. Přidejte společnost do nastavení připojení s duálním zapisováním.
3. [Zavedení](bootstrap-company-data.md) dat Dataverse pomocí třímístného kódu společnosti ISO.
4. Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.

Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Stávající instance finanční a provozní aplikace a nová instance aplikace Customer Engagement

Nastavení připojení s dvojím zapisováním mezi existující instancí finanční a provozní aplikace a novou instancí aplikace Customer Engagement probíhá v prostředí Finance a Operace.

1. [Nastavení připojení z finanční a provozní aplikace](enable-dual-write.md).
2. Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.

Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Stávající instance finanční a provozní aplikace a stávající instance aplikace Customer Engagement

Nastavení připojení s dvojím zapisováním mezi existující instancí finanční a provozní aplikace a stávající instancí aplikace Customer Engagement probíhá v prostředí Finance a Operace.

1. [Nastavení připojení z finanční a provozní aplikace](enable-dual-write.md).
2. Chcete-li synchronizovat existující data Dataverse s finanční a provozní aplikací, [zaveďte](bootstrap-company-data.md) data Dataverse pomocí třímístného kódu ISO společnosti.
3. Spusťte funkci **Počáteční synchronizace** pro tabulky, u kterých chcete synchronizovat data.

Odkazy na příklad a alternativní přístup najdete v části [Příklad](#example).

## <a name="example"></a>Příklad

Příklad viz [Povolení Customers V3 — mapa tabulek kontaktů](enable-entity-map.md#enable-table-map)

Alternativní přístup založený na objemech dat v každé entitě, která musí spustit počáteční synchronizaci, najdete v části [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]