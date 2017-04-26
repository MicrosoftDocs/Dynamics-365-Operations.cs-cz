---
title: "Nastavit a spravovat obrázky pro moderní Retail POS"
description: "Tento článek popisuje kroky, které jsou zapojeny do vytváření a správa bitových kopií pro různé entity, které se objeví v maloobchodní moderní POS (MPOS)."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dbcf6d2ca3a6009c1631636309ff55cebb0551e6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Nastavit a spravovat obrázky pro moderní Retail POS

[!include[banner](includes/banner.md)]


Tento článek popisuje kroky, které jsou zapojeny do vytváření a správa bitových kopií pro různé entity, které se objeví v maloobchodní moderní POS (MPOS).

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Nastavení základní adresy URL média a definování šablon média ke konfiguraci formátu adresy URL pro obrázek
-------------------------------------------------------------------------------------------------

Obrazy, které se objeví v maloobchodní moderní POS (MPOS) musí být uložen externě, mimo 365 Microsoft Dynamics pro operace - Retail. Standardně jsou umístěny v systému správy obsahu, sítě dodávky obsahu (CDN) nebo serveru médií. MPOS pak prostřednictvím přístupu k cílové adrese URL načte a zobrazí obrázky odpovídajících entit, jako jsou například výrobky a katalogy. K načtení těchto externě hostovaných obrázků MPOS je zapotřebí správný formát adresy URL pro obrázky. Požadovaný formát adresy URL pro obrázky lze konfigurovat pomocí nastavení hodnoty **základní adresy URL média **v kanálu profilu a používáním funkce **šablony definování médií **pro každou entitu. Standardní formát adresy URL pro podmnožinu entit je rovněž možné přepsat pomocí funkce **úpravy v aplikaci Excel**. **Důležitá poznámka:** v aktuální verzi Dynamics 365 pro operace lze již nastavíte formát adresy URL pomocí **obraz** MPOS v atributu XML **výchozí** skupina atributů u entit. Pokud se seznámíte s Microsoft Dynamics AX 2012 R3 a nyní pomocí aktuální verze Dynamics 365 pro operace, přesvědčte se, zda vždy použít nové **šablony definovat media** funkce pro nastavení obrázků. Není možné použít nebo upravit atribut **obrázku** ve **výchozím** skupině atributů pro všechny entity včetně produktů. Změny prováděné přímo ve **výchozí** skupině atributů pro obrázky se neodrazí. Tato možnost bude zakázána v budoucích verzích. V následujících procedurách jsou obrázky nastaveny jako příklad pro entitu katalogu. Tyto postupy vám pomůžou zajistit, že správná cílová cesta obrázků je implicitně nastavena pro všechny obrázky katalogu používající obecnou cestu. Například jestliže jste externě nastavili server médií nebo CDN a chcete, aby se obrázky zobrazily v MPOS pro daný obchod, funkce **Definovat šablonu média** vám usnadní nastavení cesty umístění, kde MPOS může vyhledat a získávat obrázky. **Poznámka:**Pro tento příklad ukázkových dat je nasazen server médií na serveru maloobchodu. Však může toto mít kdekoli mimo 365 Dynamics pro operace.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Nastavení základní adresy URL médií pro kanál

1.  Otevřete 365 Dynamics HQ provoz portálu.
2.  Klepněte na tlačítko **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**kanál profily**. [![kanál profile1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  V profilu kanálu, který váš obchod používá pro MPOS aktualizujte pole **Základní adresu URL média** se základní adresou URL serveru média nebo CDN. Základní adresa URL je první část adresy URL, která je sdílena všemi složkami obrazu různých subjektů. [![profile2 kanálu](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Definování šablon médií pro entitu

1.  Klepněte na tlačítko **maloobchodní a commerce**&gt;**Správa katalogu**&gt;**katalog obrazů**.
2.  Na stránce **Obrázky katalogu** v podokně akcí klepněte na příkaz **Definovat šablonu média**. V dialogovém okně **Definovat šablonu média** v poli **Entita**, má být výchozí nastavení na **Katalog**.
3.  Na pevné záložce **Cesta média** zadejte zbývající cestu k místu obrázku. Cesta média podporuje **LanguageID** jako proměnnou. Například pro ukázková data můžete vytvořit složku **Katalogy** pro všechny katalogové obrázky na základní adrese URL médií pro váš serveru médií (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Můžete pak mít složku pro každý jazyk, jako je například en-US nebo fr-FR a zkopírovat příslušné obrázky do každé složky. Pokud nemáte různé obrázky pro různé jazyky, můžete vynechat proměnnou **LanguageID** ze své složkové struktury a poukázat přímo na složku katalogů, která bude obsahovat katalogové obrázky. **Poznámka:** Aktuální verze aplikace Dynamics AX podporuje token **{LanguageId}** pro katalog, produkt a entity katalogu. (Token **{LanguageID}** není podporován pro odběratele a jednotky pracovníků, podle existujícího standardu, který byl platná od verze aplikace Microsoft Dynamics AX 6.x.)
4.  Pro obrázky je formát názvu souboru pevně zakódován do názvu katalogu a nemůže být změněn. Z tohoto důvodu přejmenujte své obrázky, aby měly odpovídající katalogové názvy, abyste si zajistili, že je MPOS zpracovávají správně.
5.  V poli **Přípona souboru** vyberte očekávané přípony názvu souboru, v závislosti na typu obrázku, které máte. Například pro ukázková data jsou katalogové obrázky nastaveny na příponu .jpg. (Obrázkové soubory také přejmenujte tak, aby měly katalogové názvy.)
6.  Click **OK**.
7.  K ověření, zda šablony média pro obrázky byly uloženy správně, na stránce **Katalogové obrázky** klepněte znovu na **Definovat šablonu média**. K ověření šablony, aniž byste zavřeli dialogového okno **Definovat šablonu média** můžete použít pevnou záložku **Generovat adresy URL obrázku pro Excel**. Zkontrolujte vzhled adresy URL obrázku, ověřte, že adresa URL odpovídá standardu šablony, uvedenému výše. Dialogové okno **Definovat šablonu média** je nyní implicitně nastaven na cestu k obrázku pro všechny katalogové obrázky, které používají tuto běžnou cestu URL. Tato cesta URL se vztahuje na všechny katalogové obrázky do doby, než budou přepsány. První část cesty obrázku je převzata ze základní adresy URL média, které jste definovali v profilu kanálu. Zbývající část cesty je převzata z cesty, kterou jste definovali v šabloně média. Obě části jsou spojeny, aby poskytly úplnou adresu URL obrázku skladového místa. Například katalog v ukázkových datech je nazván Fabrikam Base Catalog. Název proto musí být Fabrikam Base Catalog.jpg, aby byl používán název katalogu a přípona souboru .jpg, která je nastavena do šablony. V takovém případě po zřetězení bude adresa URL https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Spusťte úlohy synchronizace pro zadání nové šablony do databáze kanálů, aby MPOS mohl šablonu použít pro přístup k obrázkům.
9.  Aktualizace šablony médií pro obrázky v katalogu na straně kanálu, je nutné spustit **úlohu 1150 katalogů** z **Retail IT**&gt;**plán distribuce**. [![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Náhled obrázku z úrovně entity
1.  Ze stránky pro položky entit v centrále můžete zobrazit náhled obrázku, který používá adresa URL obrázku odvozenou ze šablony média. V tomto případě přejděte na příslušný katalog a v podokně akcí klepněte na tlačítko **Media**&gt;**obrazy**. Chcete-li vybrat jiné obchody, které mohou mít různé profily kanálů, použijte rozevírací seznam.
2.  K úpravě nebo odstranění šablony implicitního média, se musíte vrátit do dialogového okna **Definovat šablonu média** pro stránku **Katalogové obrázky**.
3.  Lze použít tlačítka **Přidat** a **Odebrat** pro ruční změnu cesty, která je založena na implicitní šabloně a je využívána pro konkrétní obrázek. Další informace naleznete v části „Přepsání šablony médií pro položky entit“ v další části tohoto článku.
4.  Po jste dokončení náhled obrázku a jakýchkoli změn vyžadují, spusťte instanci MPOS pro příslušné úložiště a zobrazit, zda jsou zobrazeny obrázky katalogu. [![catalog4](./media/catalog4.png)](./media/catalog4.png)

**Poznámka:** Stejný postup lze použít pro všech pět entit, které jsou podporovány: pracovníka, odběratele, katalog, kategorie a produkty. „Katalogové produkty“ (produkty, které jsou nastaveny na úrovni katalogu) a „Produkty kanálu“ (produkty, které jsou nastaveny na úroveň kanálu) používají šablonu média, která je nastavena pro entitu produktů. Pro šablonu médií produktů můžete vybrat číslo obrázků produktů, které mají být zobrazeny po produktu. Můžete také nastavit pro daný produkt výchozí obrázek. Tímto způsobem lze zabránit prázdným obrázkům v MPOS a pomoci řídit, který obrázek se používá jako výchozí obrázek vyráběnou položku. V následujícím příkladu má každý produkt pět obrázků a první obrázek je nastaven jako výchozí obrázek. Varianty produktů jsou zpracovány stejným způsobem jako hlavní produkty. Název souboru obrazového souboru má být založen na čísle produktu. Některé znaky také unikly, zatímco byl vytvářen název souboru. Je tedy dobré ověřit název souboru za použití oddílu **Generovat adresy URL obrázku pro Excel**. [![bodce](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Úlohy pro synchronizaci k odeslání šablony média na stránku kanálu
Pro všech pět podporovaných entity (pracovníka, Zákazník, katalog, kategorie a produkty), při každé aktualizaci **šablony definovat media** dialogové okno nastavení obrázku, ujistěte se, spusťte úlohu katalogu (1150) z **Retail IT**&gt;**plán distribuce**. Tato úloha umožní synchronizaci aktualizované šablony médií ke kanálu a její používání MPOS. Spustíte úlohu katalogu (1150) po provedení následujících změn:

-   Aktualizovat šablonu katalogu obraz média z **katalog obrazů**&gt;**šablony definovat media**.
-   Aktualizace šablony médií obrázek zaměstnance z **zaměstnance obrazy**&gt;**šablony definovat media**.
-   Aktualizace šablony zákazníka obraz média z **obraz zákazníka**&gt;**šablony definovat media**.
-   Aktualizace šablony produktu obraz média z **obrázky produktů**&gt;**šablony definovat media**.
-   Aktualizace šablony kategorie obraz média z **kategorie obrazy**&gt;**šablony definovat media**. Také musíte publikovat kanál.

## <a name="overwriting-the-media-template-for-entity-items"></a>Přepsání šablon médií pro položky entity
Jak jste se již dozvěděli v předchozím oddílu, šablona média dané entity podporuje pouze jednu společnou cestu. Tato cesta je založena na základní adrese URL média, která je nakonfigurovaná a cesty média, která je definována. Nicméně v mnoha případech maloobchodní prodejce chce používat obrázky z různých zdrojů pro podmnožinu položek v entitě. Například obchod používá vlastní hostovaný server médií pro jednu sadu obrázků katalogu, ale pro jinou sadu používá CDN adresy URL. Pro přepsání adresy URL obrázku, která je založena na šabloně médií pro obrázky entity na úrovni entity, můžete pro stránku **Náhled** použít funkce úprav a ručních úprav v aplikaci Excel.

### <a name="overwrite-by-using-edit-in-excel"></a>Přepsání pomocí úprav v aplikaci Excel

1.  Klepněte na tlačítko **maloobchodní a commerce**&gt;**Správa katalogu**&gt;**katalog obrazů**.
2.  Na stránce **Obrázky katalogu** klepněte na příkaz **Definovat šablonu média**. V dialogovém okně **Definovat šablonu média** v poli **Entita**, má být nastavení na hodnotu **Katalog**.
3.  Na pevné záložce **Cesta média** si povšimněte umístění obrázku.
4.  Na pevné záložce **Generovat adresy URL obrázku pro Excel** klepněte na tlačítko **Generovat**. **Upozornění:** Kdykoli při změně šablony média je před použitím funkcí úpravy v aplikaci Excel nutné klepnout na **Generovat**. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) nyní zobrazit náhled obrazu URL generované na základě poslední šablony uložené média. [![excel2](./media/excel2.png)](./media/excel2.png)**Poznámka:** adresy URL, které jsou generovány pro Excel, použijte cestu a konvence media šablonu, která je definována. Tyto konvence zahrnují konvence pro názvy souborů. Předpokladem je, že jste nastavili fyzické obrázky mimo aplikaci Dynamics AX a obrázky lze získat z adresy URL, která je odvozena z šablony média, kterou jste definovali dříve. Odvozené adresy URL lze přepisovat použitím funkcí úpravy v aplikaci Excel.
5.  Klepněte na **Upravit v aplikaci Excel**.
6.  Po otevření sešitu aplikace Microsoft Excel po zobrazení výzvy klepněte na tlačítko **povolit úpravu**.
7.  Po zobrazení výzvy klepněte v pravém podokně na možnost **Důvěřovat tomuto doplňku** a počkejte, až doplněk dokončí instalaci. [![Tento doplněk důvěřovat](./media/excel4.jpg)](./media/excel4.jpg)
8.  Pokud budete vyzváni k přihlášení, zadejte pověření používané pro přístup k centrále. [![Výzva k přihlášení](./media/excel5.png)](./media/excel5.png)
9.  Poté, co se přihlásíte, je třeba zobrazit seznam adres URL obrázků pro různé položky katalogu.
10. Upravujte, přidávejte a odebírejte adresy URL obrázků pro různé položky entity.
11. Pro všechny entity s výjimkou produktů je možné přepsat adresy URL obrázku. Upravte stávající adresu URL obrázku tak, aby používala novou cílovou adresu URL obrázku a aktualizujte název souboru novým názvem souboru pro soubor obrázku. Název souboru musí být jedinečný, aby pomohl zajistit, že daný záznam je jedinečný. [![Přepsání adresy URL obrázku v aplikaci Excel](./media/excel6.jpg)](./media/excel6.jpg)**Poznámka:** při přepsání adresy URL obrázku pro entity produkty pomocí úpravy funkcí aplikace Excel nebo položky stránky entity, MPOS vždy zobrazuje všechna média šablony obrázek URL a adresy URL přepsat obraz.
12. Jakmile jste ukončili provádění změn, klepněte na možnost **Publikovat v aplikaci Excel** a vytvoříte novou položku explicitního přidružení.
13. Vraťte se do centrály a klepněte na tlačítko **OK**.
14. Spusťte odpovídající úlohy synchronizace pro entitu a zkontrolujte náhled na stránce entit nebo v MPOS.

#### <a name="creating-new-records"></a>Vytvoření nových záznamů

Můžete vytvořit nové záznamy v aplikaci Excel. Ověřte však, že poskytnete správné informace. Například k vytvoření nové položky pro katalog zkontrolujte, že jsou správné ID katalogu a název katalogu, a také zadejte jedinečný název souboru. Jedinečný název souboru je velmi důležitý, protože během publikování je v aplikaci Excel ověřována jedinečnost záznamů. Nejprve zkopírujte údaje z katalogu, pro který chcete vytvořit nový záznam, a záznam zkopírujte. Musíte aktualizovat název souboru a adresa URL, protože zbývající informace budou stejné. K vytvoření nových záznamů pro položky entit produktu můžete použít stejný základní postup. Ze sešitu aplikace Excel zkopírujte existující záznam pro produkt, pro který chcete vytvořit nový záznam a poté nahraďte adresu URL obrázku a název souboru. Ujistěte se, že název souboru je jedinečný.

#### <a name="deleting-an-existing-record"></a>Odstranění existujícího záznamu

Odstranit lze pouze přepsané záznamy adresy URL obrázku. Po dokončení odstranění a synchronizace se již obrázek nebude zobrazovat na stránce **Náhled** nebo v MPOS. Záznamy URL obrázku, které jsou odvozeny ze šablony média, nelze odstranit, protože tyto záznamy jsou vždy odvozeny od šablony média.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Přepsání ze stránky náhledu úrovně entit

Pro všechny entity s výjimkou produktů, je možné přepsat adresu URL obrázku pro danou položku entity na úrovni položky entity ze stránky **Náhled**. Pro produkty můžete použít stránku entit „Produkty v katalogu“. Tento příklad ukazuje, jak přepsat obrázek v katalogu.

1.  Klepněte na tlačítko **katalogy**&gt;**Media**&gt;**obrazy**a vyberte možnost aktualizovat obrázek katalogu.
2.  Klepněte na tlačítko **Přidat**a zadejte adresu URL obrázku k přepsání adresy URL šablony média.
3.  Potřebujete-li, aby se tento obrázek zobrazil v MPOS pro katalog, můžete jej nastavit jako výchozí obrázek.
4.  Klepněte na tlačítko **OK**. Adresa URL obrázku je aktualizovaná pro tento obrázek v katalogu a zobrazuje se náhled. [![preview3](./media/preview3.png)](./media/preview3.png)
5.  Můžete také zobrazit náhled obrázku pro všechny přepsané adresy URL obrázku na stránce s galerií **Obrázky v katalogu**.

**[![Náhled 4](./media/preview-4.png)](./media/preview-4.png)Poznámka:** v současné době v galerii nezobrazuje náhledy obrazů pro média šablona URL obrázku. Pro entity katalogu, pracovníka, odběratele a kategorie, pokud uživatel explicitně poskytne adresy URL prostřednictvím této stránky, doporučujeme naznačit, který obrázek bude výchozí obrázek, protože klienty serveru maloobchodu zobrazují pouze jeden obrázek pro katalog, odběratele, pracovníka a kategorii. Pokud uživatel nezadá výchozí obrázek, systém určí výchozí obrázek a odešlete jej volajícímu maloobchodních služeb (MPOS nebo obchodní stránky).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Přepsání adresy URL obrázku pro obrázky produktů v katalogu ze stránky náhledu

Pro přepsání adresy URL obrázku pro obrázky produktů v katalogu musíte použít ze stránku **Náhled**. Nelze používat funkce úprav v aplikaci Excel.

1.  Pokud chcete přepsat obrázky produktů v úrovni katalogu, vyberte katalog, poté vyberte produkt, jehož obrázek bude přepsán.
2.  Klikněte na možnost **Atributy**.
3.  Na další stránce vyberte **Obrázek**, a pak klikněte na tlačítko **Upravit**. Stránka **Náhled** se otevře jako posuvné dialogové okno.
4.  Klepněte na tlačítko **přidat**a adresu URL obrázku přepište novou adresou URL.
5.  Klepněte na tlačítko **OK**. Nyní vidíte náhled nového obrázku a můžete jej nastavit jako výchozí obrázek.

**[![cat3](./media/cat3.png)](./media/cat3.png)Poznámka:** po přidružení kategorie obraz, publikujte kanál a spustit úlohu kanálu k zajištění zveřejnění změn do databáze kanálů.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Nastavení obrázků zobrazení v offline režimu pro MPOS.
MPOS můžete spustit v online režimu (je-li MPOS připojeno k maloobchodnímu serveru) nebo v offline režimu (pokud neexistuje maloobchodní server nebo připojení k síti, a transakce jsou uloženy v místní offline databázi). Při spuštění MPOS v offline režimu nelze získat obrázky z externího serveru obrázků pro zobrazení z maloobchodního serveru, protože se ztratilo připojení k maloobchodnímu serveru. Stále však můžete nastavit obrázky tak, aby se zobrazily při spuštění MPOS v offline režimu.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Nastavení obrázků produktů zobrazení v offline režimu pro MPOS.

Obrázky produktu, které je nutné použít v offline režimu lze nastavit odesláním požadovaného fyzického obrázku do obrázku základního produktu.

1.  Klepněte na tlačítko **řízení informací o produktech**&gt;**produkty**&gt;**produkty**.
2.  Vyberte produkt, pro který chcete nastavit offline obrázek.
3.  Klepněte na tlačítko **Upravit**a poté klepněte na šipku v pravém horním rohu, abyste zobrazili pravé podokno.
4.  Na pevné záložce **Obrázek produktu** klepněte na tlačítko **Změnit obrázek**a odešlete fyzický obrázek pro použitá vybraného produktu v offline režimu.
5.  Uložit a zavřít stránku.
6.  Při online režimu MPOS spusťte úlohu katalogu v ústředí, abyste se ujistili, že data jsou odeslána alespoň jednou do offline databáze.
7.  MPOS přepněte do offline režimu. Zobrazí se obrázek, který jste odeslali určitého výrobku v ústředí. [![offline1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Nastavení obrázků katalogu, kategorie, zaměstnance a odběratele pro zobrazení v offline režimu MPOS.

Obrázky katalogu, kategorie, zaměstnance a odběratelů, které musí být použity v offline režimu, lze nastavit přidáním požadovaného odkazu cíle obrázku do galerie a nastavením obrázku jako výchozího obrázku pro vybranou entitu.

1.  Přejděte do katalogu a potom v podokně Akce klikněte na **Media**&gt;**obrazy**.
2.  Postupujte podle části „**Přepsání ze stránky náhledu úrovně entit**“ pro přidání externí adresy URL obrázku.
3.  Označte tento obrázek jako výchozí obrázek katalogu zaškrtnutím políčka proti obrázku uvedeného v mřížce.
4.  Spusťte úlohu katalogu. Tento obrázek bude nyní použit jako offline obrázek pro tento katalog v MPOS.
5.  Postupujte podobně pro ostatní entity, jako je například kategorie, zaměstnanec a odběratel.

[![offline2](./media/offline2.png)](./media/offline2.png)    




