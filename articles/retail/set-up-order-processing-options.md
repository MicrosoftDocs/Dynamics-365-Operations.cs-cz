---
title: "Nastavení kanálu kontaktního střediska"
description: "Toto téma poskytuje informace o zpracování objednávek pro kontaktní střediska pomocí aplikace Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0d64a27aa8aed10c210ca3c2956dce67f8d634b8
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-a-call-center-channel"></a>Nastavení kanálu kontaktního střediska

[!include [banner](includes/banner.md)]

Společnost může definovat více kanálů kontaktního střediska v aplikaci Microsoft Dynamics 365 for Retail. Kanály kontaktního střediska jsou konfigurovány v **Retail** \> **Kanály** \> **Kontaktní střediska** \> **Všechna kontaktní střediska** a jsou specifické pro právnickou osobu.

Po vytvoření nového kanálu kontaktního střediska je systematicky přiřazeno číslo provozní jednotky. Vzhledem k tomu, že kontaktní střediska jsou vytvořena jako provozní jednotky, uživatelé mohou propojit kontaktní střediska s různými funkcemi aplikace Retail, jako jsou například sortimenty, katalogy a určité způsoby dodání.

Výchozí sklad lze konfigurovat v kanálu kontaktního střediska. Poté, když jsou v daném kanálu vytvořeny prodejní objednávky, automaticky se do záhlaví prodejní objednávky zapíše výchozí sklad, pokud nebyl na zákazníkovi, který je vybrán pro prodejní objednávku, definován jiný sklad. V takovém případě bude sklad odběratele zadán ve výchozím nastavení.

Uživatelé musí být napojeni na kanál kontaktního střediska, aby mohli používat funkce kontaktního střediska. Všechny prodejní objednávky, které uživatel vytvoří v aplikaci Retail, jsou automaticky přiřazeny ke kanálu kontaktního střediska tohoto uživatele. V současné době nemůže být jeden uživatel napojen na více kanálů kontaktního střediska současně.

Profil oznámení e-mailem lze též nastavit na kanálu kontaktního střediska. Profil definuje sadu šablon e-mailu použitou při odeslání e-mailu odběratelům, kteří provedli objednávku prostřednictvím kanálu kontaktního střediska. Spouštěče e-mailu lze konfigurovat proti systémovým událostem, jako je například odeslání objednávky nebo dodávka objednávky.

Než může být proces zpracován správným způsobem prostřednictvím kanálu kontaktního střediska, musí být pro kanál definovány správné [platební metody](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-payments) a způsoby dodání.

Na úrovni kanálu kontaktního střediska můžete definovat další výchozí hodnoty vztahující se na finanční dimenze, které budou napojeny na objednávky vytvořené tímto kanálem.

## <a name="options-for-order-processing-behavior"></a>Možnosti chování zpracování objednávek

Tři nastavení konfigurace kontaktního střediska mají hlavní vliv na funkce, které jsou k dispozici pro prodejní objednávky vytvořené proti tomuto kontaktnímu středisku: **Povolit dokončení objednávky**, **Povolit přímý prodej** a **Povolit kontrolu ceny objednávky**.

### <a name="enable-order-completion"></a>Povolit dokončení objednávky

Nastavení **Povolit dokončení objednávky** na kanálu kontaktního střediska má důležitý vliv na tok zpracování prodejních objednávek, které jsou zadány pro tento kanál. Pokud je toto nastavení zapnuto, všechny prodejní objednávky musí projít sadou pravidel ověření předtím, než mohou být potvrzeny. Výběrem tlačítka **Dokončit** v podokně akcí stránky prodejní objednávky spustíte tato pravidla. Všechny prodejní objednávky, které jsou vytvořeny při zapnutém nastavení **Povolit dokončení objednávky**, musí projít procesem dokončení objednávky. Tento proces vynucuje zachycení platby a logiku ověřování platby. Kromě vynucení platby může proces odeslání objednávky spustit [zjišťování podvodu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/set-up-fraud-alerts) nakonfigurované v systému. Objednávky, u kterých se nezdaří ověření platby nebo podvodu, jsou zablokovány a nelze je uvolnit k dalšímu zpracování (například výdeje nebo expedice), dokud není vyřešen problém, který způsobil zablokování.

Když je nastavení **Povolit dokončení objednávky** zapnuté pro kanál kontaktního střediska, položky řádku jsou zadány na prodejní objednávce a uživatel kanálu se pokusí zavřít nebo odejít z formuláře prodejní objednávky, aniž by nejdříve vybral **Dokončit**, systém vynucuje proces dokončení objednávky otevřením stránky shrnutí prodejní objednávky a vyžádáním, aby uživatel správně odesla objednávku. Pokud nelze objednávku správně odeslat společně s platbou, uživatel může použít funkci [blokování objednávky](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds) a objednávku zablokovat. Pokud se uživatel pokouší zrušit objednávku, musí ji správně zrušit pomocí funkce Zrušit nebo funkce Odstranit, v závislosti na funkci, kterou umožňuje zabezpečení uživatele.

Pokud je nastavení **Povolit dokončení objednávky** zapnuté pro kanál kontaktního střediska, pole **Stav platby** bude sledováno na objednávce. Systém vypočítá **Stav platby**, když je odeslána prodejní objednávka. K dalším krokům zpracování objednávky, jako je výdej a expedice, mohou se systémem pohybovat pouze objednávky, které mají schválený stav platby. Pokud jsou platby odmítnuté, příznak **nezpracovávat** bude povolen na podrobném stavu objednávky, což objednávku zablokuje do vyřešení problému s platbou.

Kromě toho, pokud je nastavení **Povolit dokončení objednávky** zapnuté, když uživatelé vytváří prodejní objednávky a jsou v režimu zadávání položky řádku, pole **Zdroj** bude k dispozici na hlavním záhlaví prodejní objednávky. Pole **Zdroj** slouží k zachycení [kódu zdroje katalogu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/call-center-catalogs) ve scénáři přímého marketingového prodeje. Tento kód pak může řídit zvláštní ceny a promoakce.

I v případě, že je nastavení **Povolit dokončení objednávky** vypnuté, uživatelé mohou i nadále použít zdrojový kód na prodejní objednávku. Je však nutné nejprve otevřít podrobnosti záhlaví prodejní objednávky pro přístup k poli **Zdroj**. Jinými slovy, je zapotřebí několika dalších kliknutí. Stejné chování se vztahuje na funkce, jako je dokončení expedice a urychleně zpracované objednávky. Tyto funkce jsou k dispozici pro všechny objednávky vytvořené v kontaktním středisku. Pokud je však nastavení **Povolit dokončení objednávky** zapnuté, uživatelé mohou nalézt konfiguraci těchto funkcí v záhlaví prodeje, když jsou v zobrazení zadávání řádku. Není nutné přejít k podrobnostem záhlaví prodejní objednávky k nalezení odpovídajících nastavení a polí.

### <a name="enable-direct-selling"></a>Povolit přímý prodej

Pokud je nastavení **Povolit přímý prodej** povoleno pro kanál kontaktního střediska, uživatelé mohou využít funkce návazného a křížového prodeje v aplikaci Retail. V tomto případě se při zadávání objednávky objeví místní okna a navrhují další produkty, které může uživatel kontaktního střediska nabídnout zákazníkovi. Nabízené produkty jsou založeny na produktu, který byl právě objednán na řádku prodejní objednávky. V současné době jsou návrhy návazného a křížového prodeje nakonfigurovány na úrovni položky na produktech nebo katalozích. Pokud je nastavení **Povolit přímý prodej** vypnuté pro kanál kontaktního střediska, místní podokna se nezobrazují při zadávání objednávky, i v případě, že byl definován platný návazný nebo křížový prodej pro objednávanou položku.

Když je nastavení **Povolit přímý prodej** zapnuté, funkce skriptů a obrázků stránky zadávání prodejní objednávky jsou rovněž zapnuté. V tomto případě je k dispozici informační panel na pravém okraji stránky během zadávání objednávky. Tento panel může zobrazit skripty, které souvisejí s obecným procesem zadávání objednávek, použitý zdrojový kód katalogu nebo skripty, které se vztahují k objednávaným položkám. Panel obrázků navíc může zobrazovat obrázek produktu pro položky, které jsou objednány, pokud byl pro položku v nastavení produktu definován obrázek.

### <a name="enable-order-price-control"></a>Povolit kontrolu ceny objednávky

Když je nastavení **Povolit kontrolu ceny objednávky** zapnuto, pouze oprávnění uživatelé mohou změnit prodejní cenu položky během zadávání objednávky. Změny musí být v rámci definovaných tolerancí. Uživatelé, kteří nemají příslušná oprávnění, musí odeslat požadavek na změnu ceny. Požadavek pak bude zpracován pomocí systémového workflow pro revizi a schválení.

## <a name="channel-users"></a>Uživatelé kanálu

Při definování kanálu kontaktního střediska je nutné propojit uživatele kanálu na kontaktní středisko. V opačném případě nelze kontaktní středisko v systému použít. Když se uživatelé přihlásí do aplikace Retail a zadávají prodejní objednávky nebo vratky na stránce, která souvisí se zadáním objednávky, jejich ID uživatele je ověřeno proti konfiguraci kanálu kontaktního střediska. Pokud je uživatel napojen na konkrétní kanál kontaktního střediska, objednávky, které vytvoří uživatel, převezmou vlastnosti a výchozí hodnoty daného kanálu.

Ve výchozím nastavení je příznak **Maloobchodní prodej** na záhlaví prodejní objednávky je zapnutý pro všechny objednávky, které uživatelé kontaktního střediska vytvoří. Objednávky poté mohou využít systémových funkcí promoakce a cen specifických pro maloobchod.

Uživatelé, kteří nejsou napojeni na kanál kontaktního střediska, používají standardní funkce zadání objednávky v aplikaci Microsoft Dynamics 365 for Finance and Operations. Objednávky, které tito uživatelé zadávají prostřednictvím formuláře pro zadání prodejní objednávky, nebudou systematicky identifikovány jako objednávky aplikace Retail. Navíc tyto objednávky zadané těmito uživateli nebudou podléhat žádným pravidlům zpracování dokončení objednávek, maloobchodní cenové logice nebo jiným ověřením objednávek, které lze definovat v konfiguraci kanálu kontaktního střediska nebo v parametrech systému kontaktního střediska.

Po dokončení konfigurace kanálu kontaktního střediska a definování uživatelů kanálu k zajištění požadovaného chování systému se ujistěte, že všechny požadované parametry kontaktního střediska jsou definovány v možnostech **Retail** \> **Nastavení kanálu** \> **Nastavení kontaktního střediska** \> **Parametry kontaktního střediska**. Ujistěte se, že související číselné řady jsou rovněž definovány.

