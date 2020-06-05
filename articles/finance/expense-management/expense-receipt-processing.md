---
title: Zpracování příjemek výdajů
description: Toto téma obsahuje informace o zpracování příjemky pomocí technologie OCR. Tato funkce je navržena pro zlepšení uživatelského prostředí při vytváření sestav výdajů v aplikaci Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378224"
---
# <a name="expense-receipt-processing"></a>Zpracování příjemek výdajů

[!include [banner](../includes/banner.md)]

Zadání výdajů bylo rozšířeno o zavedení zpracování příjemky pomocí technologie OCR. Tato funkce je navržena pro zlepšení uživatelského prostředí při vytváření sestav výdajů.

## <a name="key-features"></a>Klíčové funkce

- Název obchodníka, datum a celková částka se extrahují z příjemky.
- Tato funkce se pokusí spárovat nepřipojené příjemky k nepřipojeným výdajovým transakcím.
- Uživatelé mohou vytvářet ručně zadané výdajové transakce z příjemek.

## <a name="usage-examples"></a>Příklady použití

Pro automatické připojení příjemek, které zahrnují transakce kreditních karet při vytvoření vyúčtování výdajů, proveďte následující:

  1. Otevřete pracovní prostor **Správa výdajů**.
  2. Na kartě **Příjemky** ověřte, zda existují nepřipojené příjemky. Na kartě **Příjemky** můžete také odesílat příjemky.
  3. Na kartě **Výdaje** ověřte, zda existují nepřipojené výdaje. Správce výdajů obvykle importuje tyto výdaje od zprostředkovatele kreditních karet.
  4. Vyberte **Nová sestava výdajů**. Všimněte si, že při vytváření vyúčtování výdajů lze nyní rovněž zahrnout výdaje a příjemky. Pokud přidáte výdaje i příjemky, bude spuštěno automatické párování příjemek oproti výdajům.

Pro vytvoření výdaje nebo spárování výdaje z příjemky proveďte následující:

  1. Ve vyúčtování výdajů na kartě **Příjemky** připojte příjemku výběrem možnosti **Přidat příjemky**.
  2. V části pod odeslaným obrázkem příjemky si povšimněte možností **Vytvořit** a **Spárovat**.

      - Chcete vytvořit ručně zadanou výdajovou transakci a vyplnit hodnoty extrahované z příjemky, vyberte možnost **Vytvořit**.
      - Pokud vyberete možnost **Spárovat**, systém se pokusí spárovat existující výdaj s příjemkou.

## <a name="installation"></a>Instalace

Tato funkce se používá v kombinaci s funkcí **Sestavy výdajů v nové podobě**, která usnadňuje práci s výdaji. Tato funkce je k dispozici pouze v prostředích úrovně 2+, kterými jsou sandboxové a produkční.

Chcete-li používat tyto pokročilé možnosti výdajů, nainstalujte doplněk služby správy výdajů pro Microsoft Dynamics 365 Finance a zapněte funkce ve vaší instanci. K doplňku můžete získat přístup z projektu v Microsoft Dynamics Lifecycle Services (LCS).

1. Přihlaste se k LCS a otevřete požadované prostředí.
2. Přejděte na **Úplné podrobnosti**.
3. Vyberte **Správa** nebo přejděte na pevnou záložku **Doplňky prostředí**.
4. Vyberte možnost **Nainstalovat nový doplněk**.
5. Vyberte možnost **Služba správy výdajů**.
6. Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.
7. Vyberte **Instalovat**.

V pracovním prostoru **Správa funkcí** zapněte následující funkce:

- Sestavy výdajů v nové podobě
- Automatická spárovat a vytvořit výdaj z příjemky

Pokud tyto funkce zapnete, dojde k následujícím akcím:

- Existující pracovní prostor **Správa výdajů** je nahrazen novým pracovním prostorem.
- Bude přidána nová položka nabídky pro viditelnost pole výdajů.
- Předchozí stránku **Sestavy výdajů** můžete stále otevřít přechodem na **Správa výdajů > Moje výdaje > Sestavy výdajů**.
- Pracovní postupy a jakákoliv schválení vás stále zavedou na existující stránku sestav výdajů.
- Příjemky budou zpracovány pomocí Microsoft Azure Cognitive Services a metadata budou extrahována a přidána.
- Je přidána možnost, která umožňuje vytvořit sestavu výdajů, která obsahuje spárované nepřipojené příjemky.
- Možnost, která je přidána do sestav výdajů, umožňuje vytvořit řádek výdajů z příjemky, nebo se pokusí o spárování existující příjemky s existujícím řádkem výdajů.

Další informace o přepracované funkci sestav výdajů naleznete v tématu [Sestavy výdajů v nové podobě](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Časté dotazy

**Používá společnost Microsoft moje data pro své modely?**

Ne, společnost Microsoft vytvořila obecný model strojového učení pro svou službu zpracování příjemek. Tento model není založen na příjemkách, které jste odeslali.

**Kde je tato funkce dostupná a zpracovaná?**

V současné době jsou podporovány Spojené státy.

**Kam moje příjemky směřují?**

Aplikace Finance bude kontaktovat Cognitive Services za účelem extrahování dat polí. Služby Cognitive Services si ponechají kopii vaší příjemky po dobu 24 hodin během zpracování. Po dokončení zpracování služby Cognitive Services odstraní příjemku. Příjemky jsou stále uloženy v aplikaci Finance.

Další informace naleznete v tématu [Povolení pochopení příjemek s novou funkcí rozpoznávání formulářů](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
