---
title: Zprávy procesoru zpráv
description: Toto téma poskytuje informace o funkci zpráv procesoru zpráv pro úlohy jednotky škálování.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 76a3cc316da322c7997072c00780f2fc133bfd2a02274b1e53f5cd06cfb1277e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748852"
---
# <a name="message-processor-messages"></a>Zprávy procesoru zpráv

[!include [banner](../includes/banner.md)]

Zprávy procesoru zpráv se používají při spuštění cloudových a hranových jednotek pro [výrobní úlohy](cloud-edge-workload-manufacturing.md) a [úlohy správy skladu](cloud-edge-workload-warehousing.md).

Mezi prostředím nasazení centra a jednotky škálování se vyměňuje velké množství dat, aby byla synchronizována, ale pouze několik z těchto výměn dat bude zpracováno *procesorem zpráv*. Zprávy zpracované procesorem zpráv můžete zobrazit přechodem na **Správa systému >Procesor zpráv > Zprávy procesoru zpráv**.

## <a name="message-grid-columns-and-filters"></a>Sloupce a filtry mřížky zpráv

Můžete použít pole v horní části stránky **Zprávy procesoru zpráv** k nalezení konkrétních zpráv, které hledáte. Většina z těchto filtrů odpovídá záhlaví sloupců v mřížce zpráv. K dispozici jsou následující filtry a záhlaví sloupců:

- **Typ zprávy** – Určuje typ zprávy.
- **Fronta zpráv** – Určuje název fronty, ve které má být zpráva zpracována. K dispozici jsou následující fronty:
  - *Jednotka škálování na centrum*
  - *Centrální uzel na jednotku škálování provádění skladu*
  - *Centrální uzel na jednotku škálování provádění výroby*
- **Stav zprávy** – Určuje stav zprávy. K dispozici jsou následující stavy:
  - *Ve frontě* – Zpráva je připravena ke zpracování procesorem zpráv.
  - *Zpracováno* – Zpráva byla úspěšně zpracována procesorem zpráv.
  - *Zrušeno* – Zpráva byla zpracována, ale zpracování se nezdařilo.
- **Obsah zprávy** – Tento filtr provádí fulltextové vyhledávání obsahu zprávy. (Obsah zprávy se v mřížce nezobrazuje.) Filtr považuje většinu speciálních symbolů (například „-“) za mezery a všechny znaky mezery za logické operátory OR. T=Například toto znamená, pokud hledáte konkrétní hodnotu `journalid` rovnou „USMF-123456“, že systém najde všechny zprávy, které obsahují „USMF“ nebo „123456“, což bude pravděpodobně dlouhý seznam. Proto by bylo lepší zadat pouze „123456“ samostatně, protože to vrátí konkrétnější výsledky.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Příklad typu zprávy: Žádost o finanční aktualizaci zásob

Například **Typ zprávy** *Vyžádat finanční aktualizaci zásob* se používá k vytvoření a zaúčtování deníku počítání na centru, když pracovník používá aplikaci skladu k [registraci úpravy zásob](cloud-edge-warehouse-inventory-adjustment.md) na úloze správy skladu jednotky škálování. Protože tento konkrétní proces pochází z jednotky škálování, pole **Fronta zpráv** zobrazí hodnotu *Jednotka škálování na centrum*.

U tohoto typu zprávy úloha jednotky škálování zaznamenává zprávu jako součást operace úpravy zásob aplikace skladu. Data zprávy se poté přenesou do centra jako součást stejného procesu, jaký se používá pro [architekturu Commerce Data Exchange](../../commerce/commerce-architecture.md). Zpráva bude aktualizována, aby se zobrazila **Stav zprávy** jako *Ve frontě*. Procesor zprávy se poté pokusí zprávu zpracovat a aktualizuje **Stav zprávy** na *Zpracováno* při úspěchu nebo *Zrušeno* při selhání.

## <a name="view-the-message-log-message-content-and-details"></a>Zobrazit protokol zpráv, obsah zprávy a podrobnosti

Podrobné informace o zprávě najdete tak, že ji vyberete v mřížce a poté otevřete karty **Protokol** nebo **Obsah zprávy** pod mřížkou zpráv, kde se zobrazuje každá událost zpracování.

**Obsah zprávy** závisí na **Typ zprávy**, a proto budou mít jinou délku textu. Typický text obsahu zprávy začíná **{** a končí **}** a mezitím mají názvy polí jako `journalId` následovaný **:** a hodnotu, jako je *USMF-123456*.

Panel nástrojů na kartě **Protokol** obsahuje následující tlačítka:

- **Protokol** – Zobrazí výsledky zpracování. To je zvláště užitečné pro pochopení důvodů selhání zpracování zpráv, které mají **Výsledek zpracování** *Selhalo*.
- **Balíček** – Více operací zpracování zpráv lze spustit jako součást stejného dávkového procesu. Toto tlačítko vyberte, chcete-li zobrazit tato podrobná data. Například můžete zjistit, zda existují závislosti, které vyžadují, aby systém zpracovával určité zprávy v konkrétním pořadí.

## <a name="message-processor-batch-job"></a>Dávková úloha procesoru zpráv

Při spuštění cloudového a hranového nasazení dávková úloh *Procesor zpráv* bude automaticky vyvolána, když je vytvořena nová zpráva ke zpracování, abyste tuto úlohu nemuseli plánovat ručně.

V případě potřeby můžete k dávkové úloze přejít na **Správa systému > Procesor zpráv > Procesor zpráv**.

## <a name="manually-process-or-cancel-a-message"></a>Ruční zpracování nebo zrušení zprávy

V případě potřeby můžete zprávu ručně zpracovat nebo zrušit v závislosti na jejím aktuálním stavu. Chcete-li tak učinit, vyberte zprávu v mřížce a poté vyberte **Proces** nebo **Zrušit** v podokně Akce

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Nastavte obchodní události k doručování upozornění na neúspěšné výsledky zpracování

Kromě filtrování na hodnotu **Stav zprávy** *Zrušeno*, chcete-li zjistit neúspěšné zprávy, můžete nastavit [Obchodní akce](../../fin-ops-core/dev-itpro/business-events/home-page.md) na centru, aby vás upozornily na neúspěšné výsledky zpracování. Chcete-li tak učinit, aktivujte obchodní událost s názvem *Zpráva procesoru zprávy byla zpracována* na stránce **Katalog obchodních akcí** (**Správa systému > Nastavení > Obchodní události > Katalog obchodních událostí**).

V rámci aktivačního procesu budete vedeni k určení, zda je událost specifická pro jeden nebo všechny právnické osoby, a uvedete **Název koncového bodu**, který musí být definován jako první.

>[!NOTE]
> Poku je **Když dojde k obchodní události** nastaveno na *Microsoft Power Automate* (a ne například *HTTPS*), **Název koncového bodu** bude automaticky vytvořen v Supply Chain Management na základě nastavení *Microsoft Power Automate*.

### <a name="microsoft-power-automate-example"></a>Příklad Microsoft Power Automate

V tomto příkladu použijte **Když dojde k obchodní události** s *Microsoft Power Automate*, který posílá e-maily obsahující zprávy InfoLog a hypertextové odkazy k otevření stránky **Zprávy procesoru zpráv** pro konkrétní neúspěšnou zprávu o nasazení centra. V případě potřeby můžete přidat další logiku pro paralelní odesílání oznámení pomocí různých kanálů a kontrolu příjemců na základě dat události.

1. V [Power Automate](https://preview.flow.microsoft.com) vytvořte nový automatizovaný cloudový tok pro aktivační událost toku **Když dojde k obchodní události – aplikace Fin & Ops (Dynamics 365)** následovaný kroky **Analyzovat JSON** a **Poslat email**, jak je znázorněno na následujícím obrázku.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Automatizovaný cloudový tok Power Automate.":::

1. V kroku **Když dojde k obchodní události** můžete vyhledat nebo zadat **Instance** centra po **Kategorie** a pak **Obchodní akce** *Zpráva procesoru zprávy byla zpracována*, jak je znázorněno na následujícím obrázku.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Krok, když dojde k obchodní události.":::

1. Pro krok **Analyzovat JSON** zadejte **Schéma**, které definuje rozšířená pole. Můžete použít možnost *Stáhnout schéma* na stránce **Katalog obchodních akcí** v Supply Chain Management nebo začněte vložením příkladu textu schématu. Tento příklad textu je uveden za následujícím obrázkem.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Analyzovat krok JSON.":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. V kroku **Poslat email** můžete vybrat jednotlivá pole nebo začít vložením příkladu těla e-mailu do pole **Tělo**. Tento příklad je uveden za následujícím obrázkem.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate – krok odeslání zprávy.":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Když obchodní událost uložíte, bude automaticky aktivována a připravena k použití jako součást Supply Chain Management.
