---
title: Správa skladových zásob
description: Toto téma popisuje typy dokumentů, které můžete použít ke správě zásob.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 551a8408aa730bc1916f1c57b7cfd773966ce8bf
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606796"
---
# <a name="store-inventory-management"></a>Správa skladových zásob

[!include [banner](includes/banner.md)]

Při práci se zásobami v aplikaci Dynamics 365 for Retail a používání aplikace Retail POS je důležité poznamenat, že POS poskytuje omezenou podporu pro dimenze zásob a určité typy skladových položek.

Řešení POS nepodporuje následující konfigurace položek:

- Položky kusovníku (s výjimkou sady produktů, které používají některé součásti sady systému kusovníků)
- Položka se skutečnou hmotností
- Položky řízené dávkou

Aplikace Retail POS v současné době nepodporuje následující sledovací dimenze v POS:

- Dimenze dávkového sledování
- Dimenze vlastníka

Řešení POS poskytuje omezenou podporu následujících dimenzí. Omezená podpora označuje, že POS může nastavit některé z těchto dimenzí jako výchozí do skladových transakcí automaticky založených na konfiguraci nastavení skladu/úložiště. POS nebude plně podporovat dimenze způsobem, kterým jsou podporovány v případě ručního zadání prodejní transakce do ERP. 

- **Skladové místo** – Uživatelé nebudou mít možnost spravovat přijímací skladové místo pro položky přijaté do skladu obchodu, pokud nebylo pro obchod nakonfigurováno použití procesu řízení skladu. Pro tyto položky bude použito výchozí přijímací skladové místo definované ve skladu obchodu. Pokud byl pro obchod povolen proces řízení skladu, bude spuštěna omezená podpora, která vyzve uživatele k výběru přijímacího místa pro celou příjemku. Položky prodávané z obchodu budou vždy vyprodány z výchozího maloobchodního umístění, jak je definováno v nastavení skladu obchodu. Místo pro správu zásob vrácení lze ovládat pomocí výchozí definice skladového místa pro vrácení ve skladu obchodu nebo na základě kódů důvodu vrácení, které jsou definovány v zásadě umístění pro vrácení.
- **Registrační značka** - Registrační značky platí pouze v případě, když byla povolena možnost **Použít procesy řízení skladu** pro danou položku a sklad obchodu. Pokud jsou v POS přijaty zásoby do skladu obchodu, kde byl povolen proces řízení skladu, a skladové místo vybrané pro přijetí položky je navázáno na profil umístění, který vyžaduje řízení registrační značky, aplikace POS systematicky použije registrační značku na řádek příjmu. Uživatelé v POS nebudou mít možnost měnit ani spravovat data této registrační značky. Je-li vyžadována úplná správa registračních značek, navrhuje se, aby obchod použil mobilní aplikaci WMS nebo klienta ERP účetního systému ke správě příjmu těchto položek.
- **Sériové číslo** – Aplikace POS má omezenou podporu pro jednotlivá sériová čísla, která mají být registrována na řádku prodejní transakce pro objednávky vytvořené v POS se serializovanými položkami. Toto sériové číslo není ověřováno proti registrovaným sériovým číslům, která jsou již v zásobách. Je-li prodejní objednávka vytvořena v kanálu kontaktního střediska nebo splněna prostřednictvím ERP a více sériových čísel je registrováno k jednomu řádku prodeje v průběhu procesu plnění v ERP, tato sériová čísla nebude možné použít nebo ověřit, pokud je pro tyto objednávky vrácení zpracováváno v POS.
- **Stav zásob** - Pro položky, které používají proces řízení skladu a vyžadují stav zásob, nelze toto pole stavu v aplikaci POS nastavit nebo změnit. Výchozí stav zásob definovaný v konfiguraci skladu obchodu bude použit při příjmu položek do zásob.

> [!NOTE]
> Všechny organizace musí otestovat konfigurace položky prostřednictvím POS při vývoji nebo v testovacím prostředí před nasazením do výroby. Položky otestujte provedením pravidelných hotovostních prodejních transakcí a vytvořením zákaznických objednávek (v příslušných případech) pomocí POS s položkami. Testování musí zahrnovat spuštění úplných procesů zaúčtování výkazů v testovacím prostředí a ověření, že nedochází k potížím.
>
> Konfigurace položek způsobem, který aplikace POS nepodporuje, bez řádného testování, může způsobit neúspěch procesu zaúčtování ve výrobě bez jednoduchého způsobu opravy problémů. Přizpůsobení aplikace partnerem nebo zákazníkem může být volitelně považováno za umožnění úspěšného dokončení těchto procesů zaúčtování. Pokud nejsou potřeba přizpůsobení, musí organizace zajistit, že konfigurace produktu byla provedena způsobem, který podporují standardní procesy aplikace POS/vytvoření objednávky/zaúčtování výkazu.

## <a name="purchase-orders"></a>Nákupní objednávky

Nákupní objednávky se vytvářejí v ústředí. Pokud je maloobchodní sklad zahrnut v záhlaví nákupní objednávky, objednávku lze přijmout v obchodě pomocí řešení Modern POS (MPOS) nebo Cloud POS v aplikaci Microsoft Dynamics 365 for Retail pomocí operace **Výdej/Příjem**. Po zadání množství přijatých v obchodě do pole **Přijmout nyní** v POS pro dokument nákupní objednávky mohou být tyto údaje uloženy místně nebo potvrzeny. Uložení těchto dat lokálně nemá žádný dopad na zásoby na skladě. Ukládání by mělo být provedeno pouze v případě, že uživatel není připraven zaúčtovat příjemku do HQ a pouze potřebuje způsob, jak dočasně uložit dříve zadaná **Přijmout nyní**. Tím se uloží data z přijetí místně do databáze kanálů uživatele. Po zpracování dokumentu s použitím možnosti **Potvrdit** budou data **Přijmout nyní** odeslána do HQ a bude zaúčtována příjemka nákupní objednávky. 

## <a name="transfer-orders"></a>Převodní příkazy

Převodní příkaz může specifikovat, že konkrétní obchod je umístěním, ze kterého lze expedovat položky nebo do kterého budou zásoby přijaty. Pokud je uživatel POS expedičním skladem pro převodní příkaz, bude moci zadat množství **Expedovat nyní** z POS. Data zadaná expedičním obchodem lze uložit místně nebo je potvrdit. Při místním uložení nejsou provedeny žádné aktualizace dokumentu převodního příkazu v HQ. Ukládání by mělo být provedeno pouze v případě, že uživatel není připraven zaúčtovat dodávku do HQ a potřebuje způsob, jak dočasně uložit dříve zadaná **Expedovat nyní**. Jakmile bude obchod připraven k potvrzení dodávky, je třeba vybrat možnost **Potvrdit**. Tato možnost zaúčtuje dodávku převodního příkazu v HQ, takže přijímací sklad bude nyní schopen proti ní přijímat. 

Pokud je uživatel POS přijímacím skladem pro převodní příkaz, bude moci zadat množství **Přijmout nyní** z POS. Data zadaná přijímajícím obchodem lze uložit místně nebo je potvrdit. Ukládání by mělo být provedeno pouze v případě, že uživatel není připraven zaúčtovat příjemku do HQ a potřebuje způsob, jak dočasně uložit dříve zadaná **Přijmout nyní**. Tím se uloží data z přijetí místně do databáze kanálů uživatele. Po zpracování dokumentu s použitím možnosti **Potvrdit** budou data **Přijmout nyní** odeslána do HQ a bude zaúčtována příjemka převodního příkazu. Je důležité si uvědomit, že přijímající obchod bude omezen pouze na schopnost potvrdit množství příjmu, která jsou rovna nebo menší než dodaná množství. Pokus o přijetí množství na převodních příkazech, která nebyla dříve expedována, bude mít za následek chyby a příjemka nebude potvrzena v HQ.

## <a name="stock-counts"></a>Počty na skladě

Inventury mohou být plánované nebo neplánované. Plánované inventury zahajuje ústředí, které také určuje, které položky musí být spočítány. Ústředí vytvoří dokument inventury skladu, který lze přijmout v obchodě, kde jsou množství skutečných zásob na skladě zadána v MPOS nebo Cloud POS. Neplánované maloobchodní inventury jsou zahájeny v obchodě a množství skutečných zásob na skladě jsou aktualizována v MPOS nebo Cloud POS. Na rozdíl od plánovaných maloobchodních inventur nemají neplánované maloobchodní inventury předdefinovaný seznam položek. Po dokončení obou typů inventury budou potvrzeny a odeslány do ústředí. V ústředí bude inventura ověřena a zaúčtována jako samostatný krok.

## <a name="inventory-lookup"></a>Vyhledávání zásob

Na stránce **Vyhledávání zásob** lze zobrazit aktuální množství produktu na skladě pro více obchodů a skladů. Kromě aktuálního množství na skladě je možné zobrazit budoucí množství, které lze slíbit (ATP) pro každý jednotlivý obchod. Chcete-li tak učinit, vyberte obchod, pro který chcete zobrazit ATP, a klikněte na **Zobrazit dostupnost obchodu**.
