---
title: Úložiště záloh šablon elektronického výkaznictví
description: V tomto článku je vysvětleno použití úložiště zálohy elektronického vykazování (ER) pro obnovení šablon.
author: kfend
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.custom: 27621
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable
ms.openlocfilehash: 61e6119c50ee79d8623d1b49d273fb8c07f88944
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281895"
---
# <a name="backup-storage-of-er-templates"></a>Úložiště záloh šablon ER

[!include [banner](../includes/banner.md)]

[Přehled elektronického výkaznictví](general-electronic-reporting.md) umožňuje podnikovým uživatelům konfiguraci formátů pro odchozí dokumenty v souladu s právními požadavky různých zemí a oblastí. Konfigurované formáty ER mohou používat předdefinované šablony pro generování odchozích dokumentů v různých formátech, například sešity Microsoft Excel, dokumenty Microsoft Word nebo dokumenty PDF. Šablony jsou vyplněny daty, které vyžaduje nakonfigurovaný datový tok pro generované dokumenty.

Každý konfigurovaný formát lze publikovat jako součást řešení elektronického vykazování. Každé řešení ER lze exportovat z jedné instance financí a provozu a importovat do jiné instance.

Systém ER používá [Konfigurace správy dokumentů](../../fin-ops/organization-administration/configure-document-management.md), která uchovává požadované šablony pro aktuální instanci financí a provozu. V závislosti na nastavení architektury ER, ukládání objektů Blob Microsoft Azure nebo složku Microsoft SharePoint lze vybrat jako fyzické umístění primárního úložiště pro šablony. (Další informace naleznete v tématu [Konfigurace systému elektronického výkaznictví (ER)](electronic-reporting-er-configure-parameters.md).) Tabulka DocuValue obsahuje pro každou šablonu samostatný záznam. V každém záznamu ukládá pole **AccessInformation** cestu k souboru šablony, který je umístěn v konfigurovaném umístění úložiště.

Při správě instancí financí a provozu se můžete rozhodnout migrovat aktuální instanci do jiného umístění. Můžete například migrovat instanci výroby do nového prostředí sandbox. Pokud jste nakonfigurovali platformu ER pro ukládání šablon v úložišti objektů Blob, bude tabulka DocuValue v novém prostředí sandbox odkazovat na instanci ukládání objektů Blob v produkčním prostředí. K této instanci však nelze přistupovat z prostředí izolovaného prostoru (sandbox), protože proces migrace nepodporuje migraci artefaktů v úložišti objektů BLOB. Pokud se tedy pokusíte spustit formát ER, který používá šablonu pro generování obchodních dokumentů, dojde k výjimce a zobrazí se upozornění na chybějící šablonu. Také budete navedeni pomocí nástroje čištění ER odstranit a poté znovu importovat konfiguraci formátu ER obsahující šablonu. Vzhledem k tomu, že je možné provést několik konfigurací formátu ER, může být tento proces časově náročný.

Úložiště záloh šablon ER vám může pomoci vytvořit šablony tak, aby byly vždy k dispozici pro generování obchodních dokumentů.

> [!NOTE]
> Tuto funkci lze použít pouze v případě, že jako fyzické úložiště pro šablony ER bylo vybráno úložiště BLOB.

## <a name="automated-recovery-and-notification"></a>Automatické obnovení a oznámení

U této funkce je každá šablona nové konfigurace formátu ER v aktuálním prostředí automaticky uložena do umístění úložiště zálohy pro šablony (tabulka databáze ERDocuDatabaseStorage) v případě, že dojde k následujícím událostem:

- Importujete novou konfiguraci formátu ER, která obsahuje šablonu.
- Dokončili jste návrh verze konfigurace formátu ER, která obsahuje šablonu.

Záložní kopie šablon jsou migrovány do nové instance modulu financí a provozu jako součást databáze aplikace.

Je-li pro generování odchozích dokumentů požadována šablona formátu ER, zpracování plateb dodavatelů včetně generování avíza o platbách a kontrolních sestav, například požadovaná šablona není v umístění primárního úložiště nalezena, dojde k následujícím událostem:

- Pokud je tato šablona k dispozici v umístění úložiště zálohy, automaticky se převezme z umístění úložiště zálohy, obnoví se do hlavního umístění úložiště a použije se pro aktuální spuštění.
- Každému uživateli, který je přiřazen k roli **Návrhář elektronického výkaznictví** nebo **Správce systému**, se zobrazí upozornění na chybějící šablonu v centru akcí. Zpráva, která se zobrazí, závisí na hodnotě parametru **Automaticky spustit proceduru obnovení poškozených šablon v dávce**:

    - Je-li tento parametr nastaven na **Vypnuto**, je při spuštění dávkového zpracování doporučena automatická oprava podobných problémů pro jiné konfigurační šablony formátu ER. Zpráva obsahuje odkaz, který lze použít ke spuštění dávkového zpracování.
    - Je-li tento parametr nastaven na **Zapnuto**, zobrazí se zpráva s upozorněním, že chybějící šablony byly zjištěny a že byl automaticky naplánovaný nový dávkový proces **Obnovit poškozené šablony ze zálohy interní databáze**. Tento dávkový proces automaticky opraví podobné problémy pro ostatní šablony.

Chcete-li nastavit parametr **Automaticky spustit proceduru obnovení poškozených šablon v dávce**, postupujte dle následujících kroků:

1. Ve financích a provozu otevřete **Správa organizace \> Elektronické výkaznictví \> Stránka konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Uživatelské parametry** nastavte požadovanou hodnotu pro parametr **Automatické spuštění procedury obnovy poškozených šablon v dávce**.

> [!NOTE]
> Tento parametr je definován pro konkrétního uživatele uživatele aplikace a protokolovanou společnost.

![Stránka konfigurací elektronického výkaznictví.](./media/GER-BackupTemplates-1.png)

Na následujícím obrázku je znázorněn příklad zprávy, která se zobrazí při nastavení parametru **Automatické spuštění procedury obnovy poškozených šablon v dávce** na hodnotu **Zapnuto**.

![Stránka deníku plateb dodavatelů.](./media/GER-BackupTemplates-2.png)

Následující ilustrace znázorňuje dávkovou úlohu **Obnovit poškozené šablony ze zálohy interní databáze** na stránce **Dávková úloha**.

![Stránka Dávková úloha.](./media/GER-BackupTemplates-3.png)

Protokol spuštění s dokončenou dávkovou úlohou **Obnovit poškozené šablony ze zálohy interní databáze** obsahuje informace o šablonách, které byly obnoveny z umístění úložiště zálohy do umístění primárního úložiště.

![Stránka historie dávkových úloh.](./media/GER-BackupTemplates-4.png)

Ve výchozím nastavení je proces automatického vytváření záložních kopií šablon, které jsou umístěny v konfiguracích formátu ER, zapnutý. Chcete-li zastavit vytváření záložních kopií šablon, nastavte možnost **Zastavit vytváření záložní kopie šablony** na **Ano** na kartě **Přílohy** na stránce **Parametry elektronického vykazování**. Můžete otevřít tuto stránku z pracovního prostoru **Elektronické vykazování**.

Nastavíte-li možnost **Zastavit vytváření záložních kopií** na **Ano** a nechcete zachovat záložní kopie, které byly dříve vytvořeny ze šablon, vyberte možnost **Vyčistit úložiště záloh** na stránce **Parametry elektronického vykazování**.

Pokud jste upgradovali prostředí na finance a provoz verze 10.0.5 (říjen 2019) a chcete migrovat do nového prostředí, které obsahuje konfigurace formátu ER, které lze spustit, vyberte možnost **Naplnit úložiště zálohy** na stránce **Parametry elektronického vykazování** před tím, než dojde k migraci. Toto tlačítko spustí proces vytváření záložních kopií všech dostupných šablon, aby je bylo možné uložit do umístění úložiště záloh ER pro šablony.

![Stránka parametrů elektronického výkaznictví.](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Ruční zotavení

Přejděte na položky **Správa organizace** \> **Elektronické výkaznictví** \> **Obnovit poškozené šablony**, abyste mohli ručně spustit proces obnovení šablon ER z umístění úložiště zálohy do umístění primárního úložiště. Než tento proces zahájíte, na stránce **Obnovit poškozené šablony** můžete určit, zda bude prováděna interaktivně, nebo zda bude naplánován dávkový proces.

## <a name="supported-deployments"></a>Podporovaná nasazení

Ve financích a provozu verze 10.0.5 je ukládání záloh šablon ER k dispozici pouze v cloudových nasazeních.

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Konfigurace architektury elektronického výkaznictví (ER)](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
