---
title: Objednávky kvality
description: Toto téma popisuje, jak ručně nebo automaticky vytvářet objednávky kvality a jak s nimi pracovat při provádění kontrol a zaznamenávání výsledků testů v Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69a4a61a599f1279ec7ad68ebb20c7b4b0f37005
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571850"
---
# <a name="quality-orders"></a>Objednávky kvality

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak ručně nebo automaticky vytvářet objednávky kvality a jak s nimi pracovat při provádění kontrol a zaznamenávání výsledků testů v Microsoft Dynamics 365 Supply Chain Management.

## <a name="automatically-created-quality-orders"></a>Automatické vytvoření objednávek kvality

Systém můžete nakonfigurovat tak, aby automaticky vytvářel objednávky kvality na základě pravidel vzorkování položek. Další informace viz [Vzorkování položek řízení jakosti](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Ruční vytvoření objednávek kvality

Pokud chcete ručně vytvořit objednávku kvality, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.
1. Zvolte **Nové**.
1. V dialogovém okně **Objednávky kvality** vyberte v poli **Typ odkazu** odkaz zásob, se kterými bude vaše objednávka kvality souviset. Popis typů odkazů, které jsou k dispozici pro výběr, najdete v části [Typy odkazů objednávek kvality](#ref-types) dále v tomto tématu.

    > [!NOTE]
    > Musí být k dispozici zásoby související s vybraným odkazem. Pokud pro vybranou kombinaci typu odkazu, množství a dimenzí zásob nejsou k dispozici žádné zásoby, zobrazí se chybová zpráva.

1. Proveďte některý z následujících kroků v závislosti na hodnotě, kterou jste vybrali v poli **Typ odkazu**:

    - Pokud jste vybrali možnost **Zásoby**, nejsou vyžadovány žádné další informace o odkazu.
    - Pokud jste vybrali možnost **Prodej** nebo **Nákup**, zadejte následující informace:

        - **Výběr účtu** – uveďte odkaz na číslo odběratele nebo dodavatele.
        - **Odkaz na číslo** – uveďte odkaz na číslo prodejní objednávky nebo nákupní objednávky.
        - **Odkaz na šarži** – uveďte odkaz na konkrétní řádek prodejní objednávky nebo nákupní objednávky.

    - Pokud jste vybrali možnost **Výroba**, **Karanténa** nebo **Výroba vedlejších produktů**, v poli **Odkaz na číslo** uveďte odkaz na výrobní zakázku, dávkovou objednávku nebo číslo karanténního příkazu.
    - Pokud jste vybrali možnost **Operace postupu**, zadejte následující informace:

        - **Odkaz na číslo** – uveďte odkaz na číslo výrobní zakázky nebo dávkové objednávky.
        - **Číslo operace** – uveďte odkaz na konkrétní číslo operace postupu.
        - **Operace** – uveďte odkaz na konkrétní operaci postupu.
        - **Prostředek** – uveďte odkaz na konkrétní prostředek, který musí být použit s operací postupu.

1. V poli **Testovací skupina** vyberte skupinu testů, které je nutné provést.
1. Do pole **Množství** zadejte počet položek, které je třeba otestovat.
1. V části **Dimenze zásob** zadejte jakékoli další dimenze zásob, které jsou pro vybranou položku vyžadovány.
1. Vyberte **OK**.

Po vytvoření objednávky kvality můžete začít kontrolovat zásoby a zaznamenávat výsledky testů. Další informace o tom, jak zaznamenávat a ověřovat výsledky testů, najdete v části [Kontrola kvality zboží](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Typy odkazů objednávek kvality

Objednávky kvality se používají ke sledování podrobností o inspekcích a výsledcích testů konkrétních zásob ve vašem skladu. Objednávka kvality musí obsahovat odkaz, který představuje zdroj zásoby, která je testována. Objednávky kvality mohou souviset s následujícími typy odkazů:

- **Zásoby** – tento typ odkazu označuje, že kontrolujete zásoby, které máte k dispozici. Kontroly tohoto typu jsou obvykle náhodné nebo neplánované a provádějí se, když pracovník skladu identifikuje problém.
- **Prodej** – tento typ odkazu označuje, že kontrolujete zásoby, které souvisí s konkrétní prodejní objednávkou. Kontroly tohoto typu se obvykle týkají specifikací odběratele nebo generování certifikátu analýzy (CoA), který musí být odběrateli poskytnut jako součást dodávky. (CoA se někdy označuje také jako certifikát shody \[CoC\].)
- **Nákup** – tento typ odkazu označuje, že kontrolujete zásoby, které souvisí s nákupní objednávkou. Inspekce tohoto typu se často používají ke kontrole příchozího zboží před jeho naskladněním nebo spotřebováním ve výrobních procesech.
- **Výroba** – tento typ odkazu označuje, že kontrolujete zásoby, které souvisí s výrobní zakázkou. Inspekce tohoto typu se často používají ke kontrole dokončeného zboží před jeho naskladněním.
- **Karanténa** – tento typ odkazu označuje, že kontrolujete zásoby, které souvisí s karanténním příkazem. Karanténní příkazy jsou speciální typ objednávky, která sleduje zásoby v odděleném skladu nebo oddělené oblasti ve vašem skladu. Inspekce tohoto typu se často používají ke kontrole zboží, které odběratel vrátil nebo které bylo vloženo do karantény pro další analýzu. Z karanténních příkazů lze generovat objednávky kvality. Alternativně je lze generovat z jiných zdrojů a pak lze objednávky kvality přiřadit ke karanténním příkazům.
- **Operace postupu** – tento typ odkazu označuje, že kontrolujete zásoby, které souvisí s konkrétním krokem postupu výrobní zakázky. Inspekce tohoto typu se obvykle používají k analýze nedokončené výroby (WIP) produktu, než přejde k dalšímu kroku výrobního procesu.
- **Výroba vedlejších produktů** – tento typ odkazu označuje, že kontrolujete zásoby, které souvisí s vedlejším produktem výrobní zakázky. Inspekce tohoto typu se obvykle používají ke kontrole vedlejšího produktu dávkové objednávky před přidáním vedlejšího produktu do zásob.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Prohlížení a vytváření objednávek kvality z různých částí systému

Objednávky kvality lze vytvořit ručně. Alternativně je lze vytvořit automaticky na základě vámi definovaných přidružení kvality. Další informace o tom, jak vytvořit a spravovat automatické vytváření objednávek kvality, najdete v části [Přidružení kvality](quality-associations.md).

Na stránce objednávky kvality můžete ručně vytvořit novou objednávku kvality nebo zobrazit stav objednávky kvality, která souvisí s jiným záznamem. Existuje několik způsobů přístupu na stránku objednávky kvality.

### <a name="from-the-quality-orders-page"></a>Ze stránky Objednávky kvality

Chcete-li ručně vytvořit objednávky kvality a zobrazit všechny stávající objednávky kvality, přejděte na možnost **Řízení zásob \> Periodické úkoly \> Správa kvality \> Objednávky kvality**. Zbývající části tohoto tématu poskytují další informace o tom, jak pracovat se stránkou **Objednávky kvality**.

### <a name="from-sales-orders"></a>Z prodejních objednávek

Chcete-li pracovat s objednávkami kvality, které souvisejí s vašimi prodejními objednávkami, přejděte na možnost **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky** a poté postupujte podle některého z těchto kroků:

- Otevřete prodejní objednávku nebo ji vyberte v mřížce. Poté v podokně akcí na kartě **Vyskladnit a zabalit** ve skupině **Správa kvality** výběrem možnosti **Objednávky kvality** otevřete stránku **Objednávky kvality**. Zde můžete zobrazit, vytvořit nebo aktualizovat objednávky kvality, které souvisejí s prodejní objednávkou.
- Otevřete prodejní objednávku a poté na kartě **Záhlaví** vyberte záložku s náhledem **Obecné**. Pole **Stav objednávky kvality** zobrazuje celkový stav všech objednávek kvality, které souvisejí s prodejní objednávkou.
- Otevřete prodejní objednávku a poté na kartě **Řádky** vyberte záložku s náhledem **Řádky prodejní objednávky**. Sloupec **Stav objednávky kvality** zobrazuje stav každého řádku prodejní objednávky.

### <a name="from-purchase-orders"></a>Z nákupních objednávek

Chcete-li pracovat s objednávkami kvality, které souvisejí s vašimi nákupními objednávkami, přejděte na možnost **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky** a poté postupujte podle některého z těchto kroků:

- Otevřete nákupní objednávku nebo ji vyberte v mřížce. Poté v podokně akcí na kartě **Přijmout** ve skupině **Správa kvality** výběrem možnosti **Objednávky kvality** otevřete stránku **Objednávky kvality**. Zde můžete zobrazit, vytvořit nebo aktualizovat objednávky kvality, které souvisejí s nákupní objednávkou.
- Otevřete nákupní objednávku a poté na kartě **Záhlaví** vyberte záložku s náhledem **Obecné**. Pole **Stav objednávky kvality** zobrazuje celkový stav všech objednávek kvality, které souvisejí s nákupní objednávkou.
- Otevřete nákupní objednávku a poté na kartě **Řádky** vyberte záložku s náhledem **Řádky nákupní objednávky**. Sloupec **Stav objednávky kvality** zobrazuje stav každého řádku nákupní objednávky.

### <a name="from-production-orders"></a>Z výrobních zakázek

Chcete-li pracovat s objednávkami kvality, které souvisejí s vašimi výrobními zakázkami, přejděte na možnost **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky** a poté postupujte podle některého z těchto kroků:

- Otevřete výrobní zakázku nebo ji vyberte v mřížce. Poté v podokně akcí na kartě **Zobrazit** ve skupině **Spravovat kvalitu** výběrem možnosti **Objednávky kvality** otevřete stránku **Objednávky kvality**. Zde můžete zobrazit, vytvořit nebo aktualizovat objednávky kvality, které souvisejí s výrobní zakázkou.
- Otevřete výrobní zakázku nebo ji vyberte v mřížce. Poté v podokně akcí na kartě **Výrobní zakázka** ve skupině **Podrobnosti výroby** výběrem možnosti **Postup** otevřete stránku **Postup výroby**. Chcete-li zobrazit objednávky kvality, které souvisejí s operací postupu, postupujte jedním z těchto kroků:

    - Vyberte cílovou operaci postupu v mřížce. Poté v podokně akcí vyberte možnost **Dotazy \> Objednávky kvality**.
    - Výběrem hodnoty v poli **Číslo operace** pro cílovou operaci postupu otevřete její stránku s podrobnostmi **Postup výroby**. Na záložce s náhledem **Obecné** se v poli **Stav objednávky kvality** zobrazuje stav objednávek kvality, které se vztahují k operaci postupu.

- Otevřete výrobní zakázku a vyberte záložku s náhledem **Obecné**. Pole **Stav objednávky kvality** zobrazuje stav objednávek kvality, které souvisejí s výrobní zakázkou.

### <a name="from-quarantine-orders"></a>Z karanténních příkazů

Chcete-li pracovat s objednávkami kvality, které souvisejí s vašimi karanténními příkazy, přejděte na možnost **Řízení zásob \> Periodické úkoly \> Správa kvality \> Karanténní příkazy** a poté postupujte podle některého z těchto kroků:

- Zkontrolujte hodnoty ve sloupci **Stav objednávky kvality**. Tímto způsobem se můžete dozvědět celkový stav všech objednávek kvality, které souvisejí s každým karanténním příkazem v mřížce.
- Vyberte v mřížce karanténní příkaz a poté v podokně akcí výběrem možnosti **Objednávky kvality** zobrazte, vytvořte nebo aktualizujte objednávky kvality, které souvisejí s karanténním příkazem.

## <a name="advanced-actions-for-quality-orders"></a>Pokročilé akce pro objednávky kvality

U objednávek kvality můžete podniknout několik akcí ke správě stavu, generování dokumentů a dotazování na další podrobnosti.

### <a name="reopen-a-quality-order"></a>Znovuotevření objednávky kvality

Ve výchozím nastavení již nemůžete upravovat ani aktualizovat objednávku kvality po jejím ověření a projití testy. V některých případech však možná budete muset znovu otevřít objednávku kvality po jejím dokončení.

Pokud chcete objednávku kvality znovu otevřít, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.
1. Otevřete ověřenou objednávku kvality nebo ji vyberte v mřížce.
1. V podokně akcí vyberte možnost **Znovu otevřít objednávku kvality**.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Vytvoření certifikátu analýzy pro objednávku kvality

Certifikát pravosti je zpráva generovaná týmem pro zajištění kvality organizace. Potvrzuje, že produkt splňuje specifické předpisy nebo požadavky. Vaši odběratelé nebo zákonné úřady ve vaší geopolitické lokalitě mohou vyžadovat certifikáty pravosti. Mohou být také požadovány na základě vašeho odvětví a typu produktů, se kterými manipulujete, nakupujete, vyrábíte nebo prodáváte.

Software Supply Chain Management vám umožňuje vygenerovat certifikát analýzy z objednávky kvality. Sestava bude obsahovat výsledky všech testů pro objednávku kvality, pokud je možnost **Certifikát pro sestavu analýzy** nastavena na hodnotu *Ano*. Tuto možnost lze ve výchozím nastavení nastavit na základě testu, který definujete na stránce **Testy**. Můžete však přepsat nastavení konkrétních testů pro konkrétní objednávku kvality.

Pokud chcete vygenerovat certifikát analýzy pro objednávku kvality, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.
1. Vyberte objednávku kvality, pro kterou chcete vytvořit certifikát analýzy.
1. V podokně akcí vyberte možnost **Dotazy \> Certifikát analýzy**.
1. Na stránce **Certifikát analýzy** vyberte v podokně akcí možnost **Nový**.
1. Volitelné: V poli **Kontakt** vyberte kontaktní osobu, které by měl být certifikát adresován.
1. V podokně akcí vyberte možnost **Tisk**.
1. V dialogovém okně **Certifikát analýzy** definujte, jak má být sestava vytištěna. Poté výběrem možnosti **OK** vytiskněte sestavu na tiskárně, na obrazovku, do souboru nebo na e-mail.
1. Zavřete stránky.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Blokování nebo odblokování zásob pro objednávku kvality

Když se objednávka kvality automaticky vygeneruje z přidružení kvality, vzorkování položek, které je přiřazeno přidružení kvality, lze nakonfigurovat tak, aby blokovalo celé množství zásob odkazu, který se testuje. Další informace o vzorkování položek viz [Vzorkování položek řízení jakosti](quality-item-sampling.md).

Pokud nepoužíváte úplné blokování nebo pokud vytváříte objednávku kvality ručně, systém automaticky vytvoří záznam blokování zásob pro množství položky, která se testuje na objednávce kvality. V záznamu, který je vytvořen na stránce **Blokování zásob**, je pole **Typ blokování zásob** nastaveno na hodnotu *Objednávka kvality*.

Chcete-li zobrazit a upravit blokování zásob pro objednávku kvality, která je vybrána na stránce **Blokování zásob**, vyberte v podokně akcí možnost **Dotazy \> Blokování zásob**. Další informace naleznete v tématu [Blokování zásob](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Dotaz na podrobnosti objednávky kvality

Pomocí následujících tlačítek v podokně akcí stránky **Objednávky kvality** zobrazíte více informací o objednávce kvality nebo informací souvisejících s objednávkou kvality:

- **Dotazy \> Podrobnosti o práci** – otevřete stránku, kde si můžete prohlédnout práci ve skladu související s objednávkou kvality.
- **Dotazy \> Neshody** – otevřete stránku, kde můžete zobrazit jakékoli neshody, které souvisejí s objednávkou kvality.
- **Zásoby** – příkazy v této nabídce jsou společné pro všechny transakce zásob. Můžete je použít k zobrazení nebo aktualizaci podrobností, jako jsou transakce, zásoby na skladě, rezervace a označení.

### <a name="create-cases-related-to-quality-orders"></a>Vytváření případů souvisejících s objednávkami kvality

Můžete vytvářet případy, které souvisejí s objednávkami kvality. Tímto způsobem můžete sledovat podrobnosti o problémech a pracovat na řešení. Potom můžete použít funkce workflow správy případů k směrování případu prostřednictvím předdefinovaného obchodního procesu, abyste získali další schválení nebo získali více informací o konkrétním problému. Můžete také použít funkci článků znalostní databáze k vytvoření znalostní báze řešení pro běžné problémy.

## <a name="case-management-examples-for-quality-management"></a>Příklady správy případů pro správu kvality

### <a name="example-1"></a>Příklad 1

Pracujete pro výrobní společnost, která musí dodržovat přísné předpisy týkající se výroby regulovaných produktů, jako jsou potraviny. Objednávky kvality se používají k zaznamenávání a sledování podrobností o kvalitě položek během celého výrobního procesu. Pokud objednávka kvality neprojde konkrétními testy, může dojít k problému se zařízením. Případy se používají k následování obchodního procesu a předání problému správným technikům, aby bylo možné určit hlavní příčinu. Pro snazší sledování obchodních procesů udržuje společnost znalostní bázi o běžných problémech, které se týkají objednávek kvality a problémů se zařízením.

### <a name="example-2"></a>Příklad 2

Pracujete pro distribuční společnost, která dodává produkty, které lze přizpůsobit pro různé země a regiony. Někteří odběratelé mají přísné specifikace, které je třeba dodržovat. V opačném případě mohou vzniknout poplatky a vrácení zboží nebo vrácení peněz. Objednávky kvality používáte ke sledování podrobností o každém testu a výsledcích, které odpovídají požadavkům odběratele. Případy se používají ke kontrole a schválení podrobností certifikátu analýzy před vygenerováním a připojením dokumentu spolu s dalšími doklady o přepravě.

## <a name="additional-resources"></a>Další prostředky

- [Procesy správy kvality](quality-management-processes.md)
- [Test kvality](quality-tests.md)
- [Testovací skupiny kvality](quality-test-groups.md)
- [Přiřazení kvality](quality-associations.md)
- [Procesy správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
