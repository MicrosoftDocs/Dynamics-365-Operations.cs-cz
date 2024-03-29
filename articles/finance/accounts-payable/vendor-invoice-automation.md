---
title: Automatizace faktur pro naskenované dokumenty
description: Tento článek popisuje funkce, které jsou k dispozici pro celkovou automatizaci dodavatelských faktur, a to dokonce i faktur, které obsahují přílohy.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0449a13989bad45cf0456a2678e5724036d2af3d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070687"
---
# <a name="invoice-automation-for-scanned-documents"></a>Automatizace faktur pro naskenované dokumenty

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje datové entity, které jsou k dispozici pro celkovou automatizaci dodavatelských faktur, včetně faktur obsahujících přílohy.

Organizace, které chtějí usnadnit své procesy v oblasti závazků (AP), často identifikují zpracování faktury jako jeden z hlavních procesních oblastí, které by měly být efektivnější. V mnoha případech organizace svěřují zpracování papírových faktur nezávislým poskytovatelům služeb optického rozpoznávání znaků (OCR). Poté obdrží strojově čitelná metadata faktury spolu s naskenovaným obrázkem jednotlivých faktur. Na pomoc s automatizací je pak k dispozici řešení na poslední chvíli, které umožňuje spotřebu těchto artefaktů ve fakturačním systému. Nyní je možné vydání této automatizace na poslední chvíli prostřednictvím řešení automatizace faktury.

## <a name="solution-context"></a>Kontext řešení

Automatické řešení faktur má standardní rozhraní, které přijímá metadata faktury pro hlavičku faktury a řádky faktury, a také přílohy použitelné u faktury. Jakýkoli externí systém, který dokáže generovat artefakty vyhovující tomuto rozhraní, bude moci odesílat informační kanál k automatickému zpracování faktur a příloh.

Následující obrázek znázorňuje scénář integrace vzorku, kde se společnost Contoso stala partnerem poskytovatele služeb OCR ke zpracování faktur dodavatele. Dodavatelé společnosti Contoso odesílají faktury poskytovateli služeb e-mailem. Prostřednictvím zpracování OCR poskytovatel služby generuje metadata faktury (záhlaví a řádky) a naskenovanou kopii faktury. Vrstva integrace pak transformuje tyto artefakty tak, aby je bylo možné používat.

![Vzorový scénář integrace.](media/vendor_invoice_automation_01.png)

Předchozí scénář umožňuje několik variant v případě, že je nutná integrace faktury. Migrace dat představuje jiný příklad použití tohoto rozhraní k vytvoření faktur a příloh faktur.

### <a name="solution-components"></a>Komponenty řešení

Řešení obsahuje následující součásti:

+ Datové entity pro záhlaví faktury, řádky faktury a přílohy faktury
+ Zpracování výjimek u faktur
+ Prohlížeč příloh faktur vedle sebe

Zbývající část tohoto článku obsahuje podrobné popisy těchto komponent řešení.

## <a name="data-entities"></a>Datové entity

Datový balík je jednotka práce, které musí být odeslána, aby bylo možné vytvořit záhlaví faktury, řádky faktury a přílohy faktur. Následující datové entity se používají pro artefakty tvořících datový balíček:

+ Záhlaví faktury dodavatele
+ Řádek dodavatelské faktury
+ Příloha dokumentu faktury dodavatele

Příloha dokumentu faktury dodavatele je nová datová entita, která je zavedena jako součást této funkce. Entita v záhlaví faktury dodavatele byla upravena tak, aby podporovala přílohy. Entita řádku faktury dodavatele pro tuto funkci nebyla změněna.

Pro podrobné informace o datových balíčcích viz [Přehled správy dat](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md). Pro informace o tom, jak vytvořit datové balíčky pomocí pracovního prostoru pro správu dat, viz [Zpracování a spotřebování datových balíčků v řešení finančních a provozních aplikací Dynamics 365](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).

Chcete-li rychle generovat testovací data, která zahrnují faktury a přílohy, postupujte takto.

1. Přihlaste se k instanci.
1. Přejděte na **Závazky** > **Faktury** > **Otevřít faktury dodavatele**.
1. Vytvořte faktury, které mají řádky a přílohy.

    > [!NOTE]
    > Přílohy musí být přílohy záhlaví. V současné době entita přílohy dokumentu dodavatelské faktury nepodporuje přílohy řádků.

1. Otevřete pracovní prostor **Správa dat**.
1. Vytvořte úlohu exportu, která obsahuje záhlaví faktury dodavatele, řádku faktury dodavatele a entity příloh dokumentu faktury dodavatele.
1. Exportujte data.
1. Stáhněte exportovaná data jako balíček. Nyní můžete balíček použít k importu dat do cílových instancí pro účely testování.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Určení právnické osoby faktury

Faktury importované pomocí datových balíčků lze přidružit k právnické osobě, ke které patří, dvěma způsoby:

+ Úloha importu, která fakturu zpracovává, ji importuje do stejné společnosti, ve které byla úloha naplánována v pracovním prostoru **Správa dat**. Jinými slovy společnost úlohy určuje společnost, do které faktura patří.
+ Při odeslání datového balíčku obsahujícího faktury do aplikace Finance může volající (tedy aplikace integrace běžící mimo Finance) explicitně zmínit ID společnosti v požadavku HTTP V tomto případě bude kontext společnosti, ve kterém je úloha zpracování spuštěná v modulu Finance, přepsán a faktury jsou importovány do společnosti, která byla předána v požadavku HTTP.

> [!NOTE]
> Toto chování je standardní chování správy dat. Je zde vysvětleno v kontextu faktur jenom pro úplnost.

## <a name="exception-processing"></a>Zpracování výjimky

V situacích, kdy faktury dodavatele přecházejí do finanční a provozní aplikace prostřednictvím integrace, musí existovat jednoduchý způsob zpracování výjimek nebo neúspěšných faktur členem týmu modulu Závazky a k vytvoření čekajících faktur mimo neúspěšné faktury. Toto zpracování výjimek pro faktury dodavatele je nyní součástí financí a provozu.

### <a name="vendor-invoices-that-failed-to-import-list-page"></a>Stránka se seznamem faktur dodavatele, které se nepodařilo importovat

Stránka s novým seznamem výjimek faktur je k dispozici zde: **Závazky** > **Faktury** > **Selhání importu** > **Dodavatelské faktury, které se nepodařilo importovat**. Na této stránce se zobrazují všechny záznamy v záhlaví dodavatelské faktury z tabulky fázování entity dat záhlaví faktury dodavatele. Všimněte si, že můžete zobrazit stejné záznamy z pracovního prostoru **Správa dat**. Můžete provést také stejné akce , které jsou k dispozici ve funkci zpracování výjimek z pracovního prostoru **Správa dat**. Funkce zpracování výjimek byla optimalizována pro funkčního uživatele, což usnadňuje její používání.

![Stránka seznamu výjimek.](media/vendor_invoice_automation_02.png)

Tato stránka seznamu zahrnuje následující pole, která se dodávají prostřednictvím kanálu:

+ **Společnost** – Společnost, které faktura náleží
+ **Chybová zpráva** – chybová zpráva, kterou vydává systém správy platformy k vysvětlení, proč nelze vytvořit fakturu
+ **Číslo** – číslo faktury
+ **Účet faktury**
+ **Název** – Název dodavatele
+ **Účet dodavatele**
+ **Nákupní objednávka** – Číslo nákupní objednávky pro vybranou fakturu
+ **Datum zaúčtování**
+ **Datum fakturace**
+ **Popis faktury**
+ **Měna**
+ **Protokol**
+ **Reference na řádek** –Identifikátor, který pochází z externího systému

    > [!NOTE]
    > Odkaz na řádek není ID faktury.

Tato stránka seznamu dále obsahuje podokno náhledu, které lze použít následujícími způsoby:

+ Zobrazte celou chybovou zprávu, abyste nemuseli rozbalovat sloupec **Chybová zpráva** v mřížce.

Stránka seznamu podporuje následující akce:

+ **Upravit** – otevřete záznam o výjimce v režimu úprav, abyste mohli opravit problémy.
+ **Možnosti** – přejděte ke standardním možnostem, které jsou k dispozici na stránkách seznamů. Můžete použít možnost **Přidat do pracovního prostoru** pro připnutí stránky se seznamem výjimek jako seznamu nebo dlaždice.

### <a name="vendor-invoices-that-failed-to-import-details-page"></a>Stránka s detaily o fakturách dodavatele, které se nepodařilo importovat

Při spuštění režimu úprav se zobrazí stránka **Detaily o fakturách dodavatele, které se nepodařilo importovat** pro fakturu, která obsahuje problémy. Pokud došlo k problémům u faktury, která má přílohu, příloha se nezobrazí. Přílohu je třeba k faktuře znovu připojit.

Stránka **Detaily o fakturách dodavatele, které se nepodařilo importovat** umožňuje vytvořit čekající fakturu. Po opravě problémů na faktuře v rámci zpracování výjimky můžete výběrem tlačítka **Vytvořit čekající fakturu** vytvořit čekající fakturu. Čekající faktura bude vytvořena na pozadí. 

### <a name="shared-service-vs-organization-based-exception-processing"></a>Sdílené služby vs. zpracování výjimek organizace

Stránka seznamu výjimek podporuje standardní konstrukty zabezpečení, které pracovní prostor **Správa dat** podporuje pro zpracování záznamů fázování. Úlohu importu faktury můžete zabezpečit následujícím způsobem:

+ Podle role uživatele
+ Podle uživatelů
+ Podle právnické osoby

![Úloha importu, která je zabezpečena pomocí role uživatele a právnické osoby.](media/vendor_invoice_automation_04.png)

Pokud je pro úlohu importu faktury nakonfigurované zabezpečení, stránka seznamu výjimek toto nastavení ocení. Uživatelé budou moci zobrazit pouze záznamy výjimky faktury, které jim toto nastavení umožňuje zobrazit.

Společnost Contoso se například rozhodla pro zpracování výjimek faktury podle právnické osoby. Proto je nastavení u úlohy importu faktury nakonfigurováno tak, aby uživatel u právnické osoby A mohl zobrazit pouze výjimky faktury v právnické osobě A, zatímco uživatel v právnické osobě B může zobrazit pouze výjimky faktury v právnické osobě B. Toto nastavení umožňuje dělení zodpovědností pro správu výjimek faktury.

Společnost Contoso by se také mohla rozhodnout, že nevynutí žádné zabezpečení, takže stejní uživatelé mohou zpracovávat výjimky faktury pro všechny právnické osoby. Toto nastavení umožňuje scénář sdílených služeb pro správu výjimek faktury.

## <a name="side-by-side-attachment-viewer"></a>Prohlížeč příloh faktur vedle sebe

Na pomoc se snadným zobrazením příloh pro faktury dodavatele obsahují následující stránky, které se používají v procesu fakturace, prohlížeč formátu připojení:

+ **Ošetření výjimek**
+ Stránka **Nevyřízené faktury dodavatele** (k dispozici také v procesu kontroly faktury)
+ Stránka s dotazem **Deník faktur** (pro zaúčtované faktury)

Tady jsou hlavní funkce, které poskytuje prohlížeč příloh:

+ Zobrazte všechny typy příloh, které Správa dokumentů podporuje (soubory, obrázky, adresy URL a poznámky).
+ Zobrazte vícestránkové soubory TIFF.
+ U souborů obrázků proveďte následující akce:
  + Zvýrazněte části obrázku.
  + Zablokujte části obrázku.
  + Přidejte poznámky do obrázku.
  + Přibližte nebo oddalte obrázek.
  + Naklopte obrázek.
  + Vraťte a opakujte akce.
  + Přizpůsobte velikost obrázku.

> [!NOTE]
> Tyto akce jsou k dispozici pouze pro soubory obrázků (JPEG, TIFF, PNG a tak dále). Jakékoli změny provedené u obrázku pomocí těchto akcí jsou uloženy do souboru s obrázkem. V současné době prohlížeč příloh neobsahuje správy verzí nebo schopnosti auditu.

### <a name="default-attachment"></a>Výchozí příloha

Pokud faktura dodavatele má více než jednu přílohu, můžete nastavit jeden z dokumentů jako výchozí přílohu na stránce **Přílohy**. Možnost **Je výchozí příloha** je novou možností, která byla přidaná v rámci této funkce. Tato možnost je také vystavena v datové entitě Příloha dokumentu faktury dodavatele. Proto lze výchozí přílohu nastavit pomocí integrace.

Jako výchozí přílohu lze nastavit pouze jeden dokument. Po nastavení dokumentu jako výchozí přílohy se dokument automaticky zobrazí v prohlížeči příloh při otevření faktury. Pokud jako výchozí přílohu nenastavíte žádný dokument, v prohlížeči se při otevření faktury automaticky nezobrazí žádná příloha.

### <a name="showhide-invoice-attachments"></a>Zobrazit přílohy faktur

Na stránkách **Zpracování výjimek**, **Čekající faktura** a **Deník faktur** je k dispozici nové tlačítko, které umožňuje zobrazit nebo skrýt prohlížeč příloh.

## <a name="security"></a>Zabezpečení

Pomocí rolí zabezpečení jsou v rámci zabezpečení založeného na rolích řízeny následující akce:

+ Zvýraznění
+ Blokovat
+ Poznámky

### <a name="pending-vendor-invoices-page"></a>Stránka Čekající faktury dodavatele

Následující oprávnění poskytují přístup jen ke čtení nebo přístup pro čtení a zápis k prohlížeči příloh pro zvýrazněný blok a akce anotací:

+ **Spravovat obrázek faktury dodavatele** – toto oprávnění poskytuje přístup pro čtení a zápis.
+ **Zobrazit obrázek faktury dodavatele** – toto oprávnění poskytuje přístup pouze pro čtení.

Následující funkční oprávnění poskytují přístup jen pro čtení a zápis k prohlížeči příloh pro tyto akce:

+ **Spravovat faktury dodavatele** – Tomuto funkčnímu oprávnění je přiděleno oprávnění Spravovat obrázek faktury dodavatele.
+ **Dotaz na stav faktury dodavatele** – Tomuto funkčnímu oprávnění je přiděleno oprávnění Zobrazit obrázek faktury dodavatele.

Následující role poskytují přístup jen pro čtení a zápis k prohlížeči příloh pro tyto akce:

+ **Úředník závazků** a **Manažer závazků** – Těmto rolím je přiřazeno funkční oprávnění Spravovat faktury dodavatele.
+ **Úředník závazků**, **Manažer závazků**, **Úředník centralizovaných plateb závazků** a **Úředník plateb závazků** – Těmto rolím je přiřazeno funkční oprávnění Dotázat se na stav faktury dodavatele.

### <a name="vendor-invoice-attachment"></a>Příloha faktury dodavatele

Následující oprávnění poskytují přístup jen ke čtení nebo přístup pro čtení a zápis k prohlížeči příloh pro zvýrazněný blok a akce anotací.

> [!NOTE]
> Role, které jsou uvedeny v této části, poskytují z výroby přístup k obrázkům faktury v prohlížeči příloh jen pro čtení. Pokud role musí mít také přístup pro zápis do obrázků, můžete této roli udělit přístup pro zápis pomocí oprávnění a funkčního oprávnění, které jsou zde popsány.

+ **Udržovat obrázek entity záhlaví faktury dodavatele** – toto oprávnění poskytuje přístup pro čtení a zápis k obrázkům faktury v prohlížeči příloh.
+ **Zobrazit obrázek entity záhlaví faktury dodavatele** – toto oprávnění poskytuje přístup pouze pro čtení k obrázkům faktury v prohlížeči příloh.

Následující funkční oprávnění poskytují přístup jen pro čtení k prohlížeči příloh pro tyto akce:

+ **Spravovat faktury dodavatele** – Tomuto funkčnímu oprávnění je přiděleno oprávnění entity záhlaví Spravovat fakturu dodavatele.

Následující role poskytují přístup jen pro čtení k prohlížeči příloh pro tyto akce:

+ **Úředník závazků** a **Manažer závazků** – Těmto rolím je přiřazeno funkční oprávnění Spravovat faktury dodavatele.

Pokud role uživatele poskytuje práva pro úpravy na jakékoli stránce, bude mít ve výchozím nastavení uživatel také oprávnění pro úpravy v prohlížeči úprav pro akce zvýraznění, blokování a poznámky. Pokud však existují scénáře, ve kterých by měla mít konkrétní role oprávnění pro úpravy na stránce, ale ne v prohlížeči příloh, příslušná oprávnění v předchozím seznamu lze použít k vyřešení případu použití.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

