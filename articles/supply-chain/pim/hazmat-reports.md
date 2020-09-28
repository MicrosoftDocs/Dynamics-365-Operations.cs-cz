---
title: Nebezpečné materiály – dotazy a sestavy
description: Toto téma vysvětluje, jak pracovat s různými sestavami, které se týkají nebezpečných materiálů. Mnoho z těchto sestav je potřeba, abyste během přepravy a skladování zůstali v souladu s různými předpisy o nebezpečných materiálech.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 188c339ddf5f5c2488133924e9a0288f218f495c
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803008"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Nebezpečné materiály – dotazy a sestavy

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management poskytuje různé sestavy týkající se nebezpečných materiálů. Mnoho z těchto sestav je potřeba, abyste během přepravy a skladování zůstali v souladu s různými předpisy o nebezpečných materiálech.

Všechny tyto sestavy, kromě sestavy **Multimodální nebezpečné zboží**, používají způsob doručení definovaný pro dodávku k nalezení předpisu, který by měl být použit k tisku textu k dodávce pro dané položky. Způsob dodání je přidružen k dopravci a dopravní službě. Proto musíte nastavit dopravce a dopravní službu a propojit je se způsobem dodání. Způsob dodání závisí na předpisech pro nebezpečné materiály.

Následující obrázek znázorňuje sled aktivit, ke kterým dochází, když systém generuje sestavy o nebezpečných materiálech.

![Sled aktivit pro sestavy nebezpečných materiálů](media/hazmat-report-sequence.png "Sled aktivit pro sestavy nebezpečných materiálů")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Nastavení vytváření sestav nebezpečných materiálů

Obvykle, pokud dodáváte zboží, které obsahuje nebezpečné materiály, musíte vygenerovat specifické sestavy, které vám pomohou zachovat bezpečnost a dodržování předpisů o nebezpečných materiálech. Chcete-li nastavit sestavy, postupujte následujícím způsobem.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
2. Otevřete kartu **Sestavy**. Na záložce s náhledem **Parametr sestavy nebezpečných materiálů** nastavte následující pole.

    | Sekce | Pole | popis |
    |---|---|---|
    | Multimodální nebezpečné zboží | Kód regulace | Vyberte předpis, která by se měl použít, když a je vygenerována sestava **Multimodální nebezpečné zboží**. |
    | Omezení skladování nebezpečných materiálů | Kód regulace | Vyberte předpis, který by se měl použít při vyhodnocení míry omezení skladování. |
    | Přeprava zboží po silnici | Produkt skupiny CRM | CMR znamená „karcinogenní, mutagenní a reprotoxické látky.“ Tuto možnost nastavte na **Ano**, čímž systém nakonfigurujete tak, aby tiskl konkrétní varování a sestavy týkající se zacházení s těmito látkami. |
    | Přeprava zboží po silnici | Popis skupiny nebezpečného materiálu | Zadejte text konkrétních varování, která souvisejí s CMR a přepravou zboží po silnici. Tento text bude součástí sestavy. |
    | Prohlášení odesílatele | Upozornění | Zadejte text varovné zprávy, která by měla být vytištěna na formuláři prohlášení odesílatele (například „Varování: Nebezpečné zboží, hořlavé“). |
    | Prohlášení odesílatele | Prohlášení zápatí | Zadejte text zprávy, který by měl být vytištěn v dolní části dokumentu prohlášení o dodávce. |
    | Jazyk sestavy nebezpečného zboží | Jazyk domácí sestavy nebezpečného zboží | Vyberte výchozí jazyk pro sestavy o nebezpečných materiálech, které jsou přidruženy k vnitrostátním dodávkám. |
    | Jazyk sestavy nebezpečného zboží | Jazyk sestavy exportu nebezpečného zboží | Vyberte výchozí jazyk pro sestavy o nebezpečných materiálech, které jsou přidruženy k mezinárodním dodávkám. |

## <a name="hazardous-materials-report"></a>Sestava Nebezpečné materiály

Sestava **Nebezpečné materiály** obsahuje seznam všech položek, které byly vytvořeny a definovány tak, aby obsahovaly informace o nebezpečných zbožích. Tuto sestavu můžete použít ke sledování a kontrole informací, které musíte udržovat. Stránka sestavy obsahuje omezený výběr polí z nastavení nebezpečných materiálů. Můžete si ji však přizpůsobit a podle potřeby přidat další pole.

Chcete-li zobrazit tuto sestavu, přejděte na **Řízení informací o produktech \> Dotazy a sestavy \> Dokumentace expedice nebezpečného materiálu \> Nebezpečné materiály**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Sestava Omezení skladování nebezpečných materiálů

Sestava **Omezení skladování nebezpečných materiálů** vám umožní monitorovat úrovně zásob nebezpečných materiálů ve vašich skladech, abyste se ujistili, že zůstávají pod stanovenými bezpečnými limity. Tato omezení jsou definovány pro každý uvolněný produkt.

Chcete-li zobrazit tuto sestavu, přejděte na **Řízení informací o produktech \> Dotazy a sestavy \> Dokumentace expedice nebezpečného materiálu \> Omezení skladování nebezpečných materiálů**.

Další informace, jak nastavit omezení skladování uvolněného produktu, najdete v části [Stanovení omezení pro skladování nebezpečných výrobků](hazmat-items.md#stock-limits).

Předpisy pro omezení skladování jsou definovány na stránce **Parametry řízení skladu**. Přejděte na **Řízení skladu \> Nastavení \> Parametry řízení skladu** a poté na kartě **Sestavy** v části **Omezení skladování nebezpečných materiálů** zadejte kód předpisu. Další informace naleznete v části [Nastavení vytváření sestav nebezpečných materiálů](#set-up) výše v tomto tématu.

## <a name="verified-gross-mass-report"></a>Sestava Ověřená hrubá hmotnost

Sestava **Ověřená hrubá hmotnost** umožňuje vytisknout informace o hmotnosti dodávky.

Chcete-li vygenerovat a vytisknout tuto sestavu, přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky** a otevřete příslušnou dodávku. Poté v podokně Akce na kartě **Dodávky** ve skupině **Dokument o nebezpečných materiálech** vyberte **Ověřená hrubá hmotnost**.

## <a name="multimodal-dangerous-goods-report"></a>Sestava Multimodální nebezpečné zboží

Sestava **Multimodální nebezpečné zboží** je poskytována pro dodávky, které musí být přesunuty pomocí kombinace způsobů přepravy. Obvykle se používá, když se dodávka pohybuje nejprve po silnici a později po moři.

Chcete-li vygenerovat a vytisknout tuto sestavu, přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky** a otevřete příslušnou dodávku. Poté v podokně Akce na kartě **Dodávky** ve skupině **Dokument o nebezpečných materiálech** vyberte **Multimodální nebezpečné zboží**.

Když vygenerujete tuto sestavu, informace se uloží, abyste je mohli upravit a případně znovu vytisknout sestavu. Chcete-li upravit vytvořenou sestavu, přejděte na **Řízení skladu \> Dotazy a sestavy \> Dokumentace expedice nebezpečného materiálu \> Multimodální nebezpečné zboží** a v seznamu najděte příslušnou sestavu. Po dokončení úpravy obsahu podle potřeby vyberte **Tisk** v podokně akcí pro tisk sestavy.

## <a name="shippers-declaration-report"></a>Sestava Prohlášení odesílatele

Sestava **Prohlášení odesílatele** umožňuje tisknout informace, které souvisí s prohlášením o materiálech, které jsou součástí dodávky.

Chcete-li vygenerovat a vytisknout tuto sestavu, přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky** a otevřete příslušnou dodávku. Poté v podokně Akce na kartě **Dodávky** ve skupině **Dokument o nebezpečných materiálech** vyberte **Prohlášení odesílatele**.

## <a name="carriage-of-merchandise-by-road-report"></a>Sestava Přeprava zboží po silnici

Sestava **Přeprava zboží po silnici** se podobá přepravnímu dokladu, ale obvykle se používá pro silniční dopravu v Evropě na základě Dohody o předpisech o mezinárodní silniční přepravě nebezpečného zboží (ADR). Tato sestava používá tištěný text dodávky pro položku, pokud nenastavíte pole **Popis skupiny nebezpečných materiálů** na stránce **Parametry řízení skladu**.

Chcete-li vygenerovat a vytisknout tuto sestavu, přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky** a otevřete příslušnou dodávku. Poté v podokně Akce na kartě **Dodávky** ve skupině **Dokument o nebezpečných materiálech** vyberte **Přeprava zboží po silnici**.

Když vygenerujete tuto sestavu, informace se uloží, abyste je mohli upravit a případně znovu vytisknout sestavu. Chcete-li upravit vytvořenou sestavu, přejděte na **Řízení skladu \> Dotazy a sestavy \> Dokumentace expedice nebezpečného materiálu \> Přeprava zboží po silnici** a v seznamu najděte příslušnou sestavu. Po dokončení úpravy obsahu podle potřeby vyberte **Tisk** v podokně akcí pro tisk sestavy.

## <a name="shipment-summary-report"></a>Sestava souhrnu dodávky

Sestava **Shrnutí dodávky** poskytuje informace, které jsou shrnuty podle kategorie dopravy, která souvisí s uvolněnými položkami.

Chcete-li vygenerovat a vytisknout tuto sestavu, přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky** a otevřete příslušnou dodávku. Poté v podokně Akce na kartě **Dodávky** ve skupině **Dokument o nebezpečných materiálech** vyberte **Shrnutí dodávky**.

## <a name="bill-of-lading-report"></a>Sestava Přepravní doklad

Když je ve vašem systému zapnuta funkce nebezpečných materiálů, sestava **Prepravní doklad** obsahuje sloupec **Nebezpečné materiály**, který udává, zda náklad obsahuje nebezpečné materiály. Tato sestava je k dispozici na stránce **Všechny náklady**, jako obvykle.

## <a name="packing-list-report"></a>Sestava Dodací list

Když je ve vašem systému zapnuta funkce nebezpečných materiálů, dodací listy obsahují další informace, které se vztahují k tištěnému textu dodávky pro danou položku. Tato sestava je k dispozici na stránce **Všechny náklady**, jako obvykle.
