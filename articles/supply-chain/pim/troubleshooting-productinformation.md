---
title: Řešení potíží s informacemi o produktu
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s informacemi o produktu.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5b74c1a769b3f0c3b848a034ed3d1bab76fda7eb5d8d62f4b3608d8706c696dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778643"
---
# <a name="troubleshoot-product-information"></a>Řešení potíží s informacemi o produktu

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s informacemi o produktu.

## <a name="i-cant-delete-a-released-product"></a>Nemohu odstranit uvolněný produkt.

### <a name="issue-description"></a>Popis problému

Uvolněný produkt a všechny jeho varianty můžete odstranit, pouze pokud uvolněný produkt nemá žádné související transakce.

### <a name="issue-resolution"></a>Řešení problému

Podle těchto pokynů odstraníte uvolněný produkt nebo základní produkt.

1. Zavřete všechny otevřené transakce pro položky.
1. Snižte zásoby na 0 (nula).
1. Proveďte uzávěrku skladu.
1. Odstraňte všechny varianty produktu pro hlavní produkt, který chcete odstranit.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Mohu změnit číslo položky uvolněného produktu?

Ve většině případů nemůžete upravit čísla položek uvolněných produktů, protože tato změna způsobí poškození dat. Číslo položky můžete upravit, pouze pokud musíte opravit poškození dat způsobené předchozím přejmenováním primárního klíče tohoto uvolněného produktu, jak je uvedeno v seznamu [odstraněných nebo zastaralých funkcí pro Finance and Operations 10.0.0 s aktualizací Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Chcete-li mít možnost upravit čísla položek uvolněných produktů, [hlasujte pro tento nápad na portálu Nápady](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Na řádku kusovníku se nezadává výchozí princip vyprazdňování z produktu.

### <a name="issue-description"></a>Popis problému

Když přidáte položku do řádku kusovníku, systém nepoužívá výchozí informaci o zásadě vyprazdňování, která je pro položku nastavena. Jinými slovy, princip vyprazdňování z položky se na stránce **Řádek kusovníku** nezobrazí.

### <a name="issue-resolution"></a>Řešení problému

Pokud na řádku kusovníku určíte princip vyprazdňování, bude se vztahovat na tento řádek kusovníku. Pokud je však princip vyprazdňování prázdný nebo pokud není nastaven na řádku kusovníku, princip vyprazdňování nastavený na položce bude i nadále platit pro tento řádek kusovníku, i když se na řádku kusovníku nezobrazí.

Výchozí logika pro další funkce v Microsoft Dynamics 365 Supply Chain Management obvykle tímto způsobem nefunguje. Aktuální chování však nelze změnit. Jinak může dojít k porušení některých existujících přizpůsobení, které na to spoléhají.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Systém mi umožňuje uložit duplicitní čárové kódy pro různé položky nebo pro stejnou položku, která má různé dimenze.

Systém aktuálně nevynucuje jedinečné čárové kódy a přidání tohoto omezení by bylo zásadní změnou. Microsoft má ve skutečnosti důkaz, že by tato změna narušila některé stávající instalace zákazníků. Uvažujeme však o širší konstrukční změně, která tuto funkci v budoucnu povolí.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Při úpravě šablon záznamů položek se zobrazí následující chybová zpráva: „Nelze vytvořit umístění skladu, protože položka není na skladě. Chcete-li zboží na skladě, je třeba vybrat možnost Skladovaný produkt ve skupině modelů přidružených položek.“

### <a name="issue-description"></a>Popis problému

K tomuto problému dochází, pokud se pokusíte vytvořit šablonu pro položku, která není na skladě, pomocí těchto kroků.

1. Otevřete uvolněný produkt, který není na skladě.
1. V podokně akcí na kartě **Možnosti** zvolte **Informace o záznamu**.
1. V dialogovém okně **Informace o záznamu** vyberte **Šablona firemních účtů**.

V tomto případě se zobrazí následující chybová zpráva:

> Nelze vytvořit umístění ve skladu, protože položka není na skladě. Chcete-li zboží na skladě, je třeba vybrat možnost Skladovaný produkt ve skupině modelů přidružených položek.

### <a name="issue-resolution"></a>Řešení problému

Proces vytváření šablon produktu vyžaduje zvláštní logiku specifickou pro produkt. Proto pro tento účel nemůžete použít obecné tlačítko **Šablona účtů společnosti**. Místo toho postupujte takto.

1. Otevřete uvolněný produkt.
1. V podokně akcí na kartě **Produkt** ve skupině **Nový** zvolte **Šablona \> Vytvořit sdílenou šablonu**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Výchozí text nápovědy, který je přidán do atributů produktu, není v uvolněném produktu zadán.

Popis a text nápovědy, které jsou přidány do atributů produktu, nejsou ve uvolněných produktech viditelné nebo zadané ve výchozím nastavení. Toto chování je záměrné.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Výchozí množství, které se zadá, se liší, když je zaregistrováno z kusovníku a když je zaregistrováno z verze kusovníku.

### <a name="issue-description"></a>Popis problému

Ve výchozím nastavení, když přidáte položku do kusovníku, je množství nastaveno na 1 místo množství definovaného v poli **Min. objednané množství** na stránce **Výchozí nastavení objednávky** pro vybraný produkt. Když však přidáte položku z verze kusovníku a vyberete položku a variantu, množství, které je zadáno ve výchozím nastavení, zohlední minimální množství, které je nastaveno ve výchozím nastavení objednávky pro konkrétní dimenze.

### <a name="issue-resolution"></a>Řešení problému

Toto chování se očekává. Skutečnost, že se logika liší v kusovníku a verzi kusovníku, je známým problémem. Toto chování se nicméně nezmění, protože změna může ovlivnit mnoho různých scénářů zákazníků.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>V podrobnostech o uvolněném produktu nemohu změnit připojené obrázky, které byly nahrány z datové entity Přílohy dokumentu produktu.

### <a name="issue-description"></a>Popis problému

K tomuto problému může dojít, když připojíte obrázek k položce pomocí datová entita *Přílohy dokumentu produktu*. V takovém případě se pro položku zobrazí obrázek položky. Pokud však vyberete **Změnit obrázek**, v seznamu nahraných obrázků se nic nezobrazí. U položky se navíc nezobrazují žádné přílohy.

### <a name="issue-resolution"></a>Řešení problému

Entita *EcoResProductDocumentAttachmentEntity* (*Přílohy dokumentů produktu*) importuje přílohy dokumentů pro *produkty*, ale ne pro *uvolněné*. (Uvolněné produkty jsou také známé jako *položky* .) Chcete-li zobrazit přílohy položky na stránce **Podrobnosti o uvolněném produktu**, musíte použít místo toho entitu *EcoResReleasedProductDocumentAttachmentEntity* (*Přílohy dokumentů uvolněného produktu*).

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Konektor Microsoft Flow zobrazuje následující chybovou zprávu: „Aktualizace není povolena pro pole 'ProductNumber'.“

### <a name="issue-description"></a>Popis problému

K tomuto problému dochází, pokud se pokusíte aktualizovat pole **Číslo produktu** pomocí entity V2 *Uvolněné produkty* a Microsoft Flow.

### <a name="issue-resolution"></a>Řešení problému

Toto chování se očekává. Možnost upravovat číslo produktu uvolněného produktu byla odstraněna v Dynamics 365 Finance and Operations 10.0.0 s aktualizací Platform update 24, aby se zabránilo poškození dat. Ve výjimečných případech, kdy musíte opravit poškození dat způsobené předchozím přejmenováním primárního klíče vydaného produktu, můžete požádat podporu Microsoftu, aby toto omezení dočasně odstranila.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Nemohu vytvořit uvolněnou variantu produktu v jiné právnické osobě.

### <a name="issue-description"></a>Popis problému

Pokud se pokusíte uvolnit hlavní produkt bez variant a poté vytvořit varianty v každé právnické osobě (společnosti), jak jsou požadovány, nebudete moci uvolnit varianty pomocí návrhů variant. Varianty také nebudete moci ručně vytvořit.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. Vztahy základního produktu a dimenze, které hlavní produkt může mít, jsou udržovány na sdílené úrovni. Proto nemůžete vytvořit dostupné dimenze pro sdílený základní produkt v konkrétní právní entitě, kde jsou tyto dimenze uvolněny, a poté replikovat proces v každé právní entitě, kde jsou dimenze vyžadovány. Místo toho musíte změnit proces uvolnění, abyste se přizpůsobili navrženému procesu.

Zde je proces uvolňování produktů.

1. Vytvořte sdílený základní produkt a dimenze, které lze uvolnit právnickým osobám.
1. Uvolněte produkty právnickým osobám buď pomocí návrhů variant, nebo ručním přidáním kombinací, které by měly být uvolněny.

Alternativně můžete přímo vytvořit uvolněný produkt.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Když uvolním variantu v jiné společnosti, zobrazí se následující chybová zpráva: „Varianta produktu se zadanými dimenzemi již byla vytvořena.“

### <a name="issue-description"></a>Popis problému

Pokud již byla ve společnosti A uvolněna varianta produktu a pokusíte se ji ve společnosti B uvolnit pomocí tlačítka **Nový** na stránce **Uvolněné varianty produktu**, zobrazí se následující chybová zpráva:

> Varianta produktu s určenými dimenzemi již byla vytvořena.

### <a name="issue-resolution"></a>Řešení problému

Tlačítko **Nový** na stránce **Uvolněné varianty produktu** vytvoří variantu a uvolní ji v kontextu společnosti. Pokud již byla varianta vytvořena, nemůžete použít tlačítko **Nový** pro uvolnění v jiné společnosti.

Chcete-li problém vyřešit, otevřete stránku **Základní produkt** a vyberte **Uvolnit produkt** pro uvolnění stávající varianty v požadované společnosti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]