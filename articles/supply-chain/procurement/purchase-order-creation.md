---
title: "Vytváření nákupních objednávek"
description: "Tento článek popisuje proces a možnosti při ručním vytvoření nákupní objednávky."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: fbf5337ac41ceae6e911c056db5226c8ed1cefb0
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017

---

# <a name="create-purchase-orders"></a>Vytváření nákupních objednávek

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tento článek popisuje proces a možnosti při ručním vytvoření nákupní objednávky.

Při vytvoření nákupní objednávky proběhne zadání obecných informací o celé objednávce v záhlaví nákupní objednávky. Poté můžete přidat jeden nebo více řádků do nákupní objednávky. Tento článek popisuje některé z nejčastěji používaných možností, které jsou k dispozici.  

Nákupní objednávky můžete vytvořit také zkopírováním řádků z jiného dokumentu nákupní objednávky nebo prodejní objednávky. V takovém případě můžete obrátit znaménko u zásob, stejně jako byste obrátili znaménko na faktuře a označili připsání na stranu Dal.  

I když můžete nákupní objednávky vytvořit ručně, jsou obvykle generovány z jiných procesů. Objednávky lze automaticky vytvořit podle jiných dokumentů, jako jsou žádanky. Případně je lze vytvořit jako součást hlavního plánování procesu prostřednictvím plánovaných nákupních objednávek. Pokud používáte nákupní smlouvy, lze nákupní objednávky vytvořit pomocí akce **Dílčí objednávka**. K dispozici jsou také rozšířené metody pro automatické vytvoření nákupní objednávky. Objednávky lze například vytvořit při použití přímé dodávky nebo řetězů mezipodnikové objednávky.

## <a name="creating-a-purchase-order-header"></a>Vytvoření záhlaví nákupní objednávky
Při vytvoření nové nákupní objednávky se zobrazí dialogové okno, kde můžete zadat nejběžnější informace pro záhlaví nákupní objednávky. Po klepnutí na tlačítko **OK** se zavře dialogové okno, je vytvořena objednávka, a vy můžete zadat další informace do záhlaví.  

První podrobností, které je nutné zvážit při vytváření nákupní objednávky, je typ objednávky. Typ **Nákupní objednávky** se používá nejčastěji. Pokud jsou však potřeba opravné faktury, můžete použít typ **Vratka**.  

Je nutné určit dodavatele v poli **Účet dodavatele**. Pro toto pole můžete hledat název účtu nebo název dodavatele. Pokud dodavatel doručuje z více umístění, ale používá jeden fakturační účet, můžete vybrat daný účet faktury v poli **Účet faktury** a poté ji používat s účty různých dodavatelů. Pokud je nutné vytvořit nákupní objednávky pro produkty, které nebudete objednávat opakovaně, můžete použít možnost **Jednorázový dodavatel**. Tato možnost automaticky vytvoří nový účet dodavatele, který je označen jako jednorázový účet, a umožní tak jednodušší pozdější pročištění pro jednorázové účty v modulu **Závazky**. Pokud jste vybrali účet dodavatele, mnoho polí v hlavičce nákupní objednávky dědí výchozí hodnoty z informací, které jsou přidruženy k účtu dodavatele. Například výchozí pracoviště pro doručení a sklad jsou zkopírovány z informací o dodavateli. Můžete však přepsat tyto výchozí hodnoty, je-li nákup určen pro jiné umístění.  

Pokud dodavatel poskytl referenční číslo objednávky, můžete zaznamenat tyto informace v poli **Odkaz dodavatele**. Pro vrácené objednávky je nutné zadat hodnotu v poli **RMA** a vytvořit tak odkaz na autorizaci dodavatele pro zpracování vratky.  

Pokud je nákupní smlouva spojena s objednávkou, je třeba zadat tyto informace v poli **Nákupní smlouva**.  

Záhlaví nákupní objednávky obsahuje také informace o nákladech, které platí pro celou objednávku, namísto pro jednotlivé řádky. Poplatky lze automaticky přidán k objednávce, pokud byly nastaveny automatické náklady pro dodavatele nebo skupinu nákladů dodavatele. Náklady v záhlaví objednávky lze přidávat také ručně klepnutím na možnost **Spravovat náklady** v podokně akcí.

## <a name="adding-purchase-order-lines"></a>Přidání řádků nákupní objednávky
Nákupní objednávky mohou být pro fyzické produkty nebo služby. Nastavení skupiny modelů zásob určuje, zda se specifické číslo položky vztahuje na produkt nebo službu. Zboží, které je nakoupeno, je obvykle určováno číslem položky. Nicméně pokud je objednávka pro produkty nebo služby, které jsou spotřebovány přímo, můžete nastavit položku také pomocí kategorie zásobování.  

Řádky nákupní objednávky obsahují velký počet polí, ale mnoho z těchto polí mají výchozí hodnotu nebo hodnotu, která je zděděna ze záhlaví objednávky. Další pole jsou nastaveny při výběru produktu nebo služby. Pole, která se často nastavují ručně, zahrnují pole pro číslo položky, množství a požadované datum dodávky. Informace o jednotkové ceně a slevách jsou také velmi důležité, ale hodnoty těchto polí jsou často určeny obchodními nebo nákupními smlouvami.  

Při výběru produktu můžete hledat celý název produktu nebo jeho část namísto čísla položky. Pokud má výrobek několik variant, jako jsou různé velikosti, zobrazíte přehled dostupných variant pomocí funkce **Přidat řádky** nebo pomocí vyhledávání, které je k dispozici v poli **Číslo varianty**.  

Často bude nutné určit několik dimenzí pro vybranou položku na každém řádku nákupní objednávky. Dimenze, které je nutné zadat, závisí na skupinách dimenzí, které byly přiřazeny k definici hlavního produktu. Například často musíte zadávat pracoviště a sklad a označit tak umístění, kam je třeba produkt doručit. Varianty produktu zjistíte zadáním čísla varianty, nebo zadáním hodnot pro jednu nebo více dimenzí produktu, jako je například barva, velikost, konfigurace nebo styl. Sledování dimenzí, jako například dávek a sériových čísel, umožňuje jednoznačnou identifikaci každé šarže zásob. Po vytvoření objednávky můžete zachytit hodnoty dimenze v objednávce pomocí akce **Registrace**. Například můžete mít objednáno pět kusů zboží. Později zaregistrujete, že tři z těchto dílů budou černé, a dva z nich budou modré. Tento přístup je alternativou k zachycení informací o dimenzi během registrace příchodu.  

Můžete zkontrolovat podrobnosti o stavu skladové transakce pro produkty, které jsou skladem. Můžete například zkontrolovat zásoby na skladě, které vám pomohou rozhodnout se, kolik kusů je třeba objednat. Případně můžete zkontrolovat stav zásob pro objednané množství a zjistit tak, zda došlo k příchozí registraci při doručení.  

Řádek nákupní objednávky, který slouží k vrácení produktu dodavateli, bude mít záporné množství. Konkrétní šarži pro vrácení můžete vybrat pomocí akce **Rezervace**.  

V některých případech můžete chtít rozdělit objednané množství tak, aby jeho různé části byly dodávány v různých termínech. Tyto dodávky lze nastavit pomocí akce **Plán dodávek**, která je k dispozici v nabídce **Řádek nákupní objednávky** v zobrazení **Řádky**.  

Poplatky lze automaticky přidán k řádkům nákupní objednávky, pokud byly nastaveny automatické náklady pro dodavatele nebo skupinu nákladů dodavatele a pro položku nebo skupinu nákladů na položku. Nicméně více obvyklé je ruční přidání poplatků na úrovni řádku objednávky. Chcete-li přidat poplatek, otevřete stránku **Udržovat náklady** pomocí akce **Udržovat náklady** v nabídce **Finance** v zobrazení **Řádky**. Výhodou přidání poplatků přímo na úrovni řádku objednávky je to, že poplatek může být přidělen jako náklady skladu. Chcete-li nastavit kódy poplatků pro zaúčtování ceny produktu, použijte debetní možnost **Položka**. Tyto typy nákladů musí být přiděleny ze záhlaví nákupní objednávky k řádkům předtím, než může být objednávka potvrzena. Můžete například přidělit náklady na základě množství na každém řádku. Kategorie nákladů také ovlivňuje to, jak jsou poplatky účtovány. Například pevné náklady určují pevnou částku a procentuální náklady se vypočítají jako procento z čisté částky na řádku objednávky. Nákupní objednávky lze přiřadit k vytížení a vytížení může obsahovat odhad očekávaných výdajů za náklady na dopravu. Tyto náklady lze přidělit z vytížení zpět na řádky nákupní objednávky.

## <a name="purchase-order-actions"></a>Akce nákupní objednávky
Po přidání záhlaví a řádků do nákupní objednávky musíte často dokončit další kroky ještě předtím, než je objednávka připravena pro potvrzení. Vzhledem k tomu, že je k dispozici mnoho možností, může pro vás užitečné použít [Akci hledání](/dynamics365/unified-operations/fin-and-ops/get-started/action-search) a najít s její pomocí odpovídající položku.  

Produkty lze nastavit na objednávce tak, že mají doplňkové položky. Doplňkové položky jsou výrobky, které musí nebo mohou být nakoupeny společně s jinými přípravky. Doplňkové produkty mohou být přidány zdarma nebo za poplatek jako doprovodné produkty, nebo je možné se rozhodnout, zda je chcete přidat do objednávky, nebo nikoliv. Po přidání každého řádku objednávky můžete zkontrolovat doplňkové položky. Nicméně pravděpodobně je vhodnější zkontrolovat a přidat příslušné doplňkové položky pro všechny řádky na stránce **Doplňkové položky**, kterou lze otevřít z podokna akcí.  

Slevy jsou obvykle přidávány na řádky ihned, jak jsou vytvořeny. Nicméně několik slev se však vztahuje na celou objednávku:

-   Akce **Celkové slevy** vypočítá procento celkových slev, které se aplikuje na celou objednávku. Nepleťte si tuto slevu s procentem platební slevy. Platební slevy jsou použity, pokud je faktura zaplacena, a jsou závislé na vyrovnání platby k určitému datu.
-   Pokud se používají víceřádkové slevy, je nutné pro výpočet a přiřazení k objednávce použít akci **Víceřádkové slevy**. Víceřádkové slevy jsou slevy, které lze nabídnout, pokud kombinace produktů v objednávce překročí společný práh. Tento typ slev využívá pouze několik společností.

Poplatky se svým kódem, který používá debetní typ **Položka**, musí být přiřazeny k úrovni řádku, aby mohla být objednávka potvrzena. Může pro vás být vhodné přiřadit tyto náklady na úrovni záhlaví objednávky, abyste tak mohli zadat celkovou výši poplatku. V takovém případě však musí být náklady přiděleny na každý řádek, aby mohla být objednávka potvrzena. Můžete použít akci **Přidělit náklady** a rozdělit tak částky z poplatků, které jsou přiřazeny na úrovni záhlaví mezi řádky objednávky. Náklady lze rozdělit podle čisté částky každého řádku v souladu s množstvím, které bylo objednáno, nebo rovnoměrně mezi řádky objednávky. Poté, co přidělíte náklady k řádkům, se poplatek odebere ze záhlaví objednávky.  

Nákupní objednávky lze nakonfigurovat tak, aby vyžadovaly, aby byly rozpočtové prostředky přiděleny k objednávce, než bude možné objednávku zpracovat. V takovém případě můžete použít akci **Kontrola rozpočtu** a rozpočet přidělit.  

Bude pravděpodobně nutné zpozdit dokončení nákupní objednávky. Například můžete vyžadovat další informace o produktech nebo službách, nebo může být pravděpodobně nutné získat povolení pro výdaj. Existuje několik způsobů pro pozdržení objednávky. Například můžete počkat na potvrzení objednávky. Navíc pokud používáte pracovní postup pro změny, neodesílejte objednávku ke schválení. Pokud zablokujete všechny objednávky pro určitého dodavatele, můžete označit dodavatele jako **Blokováno** a umožnit tak zpracování u hlavního dodavatele. Existují okolnosti, které by mohly bránit zpracování objednávky. Zpracování například může být zakázáno, pokud byly překročeny limity úvěru, nebo pokud nejsou k dispozici rozpočtové prostředky.

<a name="see-also"></a>Viz také
--------

[Přehled nákupních objednávek](purchase-order-overview.md)

[Potvrzení a odmítnutí nákupní objednávky](purchase-order-approval-confirmation.md)

[Příjem produktů proti nákupním objednávkám](product-receipt-against-purchase-orders.md)

[Přehled faktur dodavatele](/dynamics365/unified-operations/financials/accounts-payable/vendor-invoices-overview)




