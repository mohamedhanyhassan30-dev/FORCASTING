import { useMemo, useRef, useState } from 'react';
import Header from '@/components/Header';
import InputForm from '@/components/InputForm';
import ResultsView from '@/components/ResultsView';
import { CalcInput, calculate, FullResult } from '@/lib/calculator';
import { loadBenchmarks } from '@/lib/industries';
import { exportPdf } from '@/lib/pdf';
import { toast } from 'sonner';

const Index = () => {
  const [clientName, setClientName] = useState('');
  const [input, setInput] = useState<CalcInput>({
    industry: 'clinic',
    budget: 1000,
    country: 'sa',
    hasOffers: true,
    hasSocialProof: false,
  });
  const [result, setResult] = useState<FullResult | null>(null);
  const resultsRef = useRef<HTMLDivElement>(null);

  const onCalculate = () => {
    if (!input.budget || input.budget <= 0) {
      toast.error('من فضلك أدخل ميزانية شهرية صحيحة');
      return;
    }
    const bm = loadBenchmarks();
    const r = calculate(input, bm);
    setResult(r);
    setTimeout(() => resultsRef.current?.scrollIntoView({ behavior: 'smooth', block: 'start' }), 100);
  };

  const onExport = () => {
    if (!result) return;
    try {
      exportPdf(input, result, clientName);
      toast.success('تم تحميل التقرير');
    } catch (e) {
      toast.error('حدث خطأ أثناء توليد التقرير');
    }
  };

  return (
    <div className="min-h-screen">
      <Header />
      <main className="max-w-4xl mx-auto px-4 sm:px-6 py-10 space-y-8">
        {/* Hero */}
        <section className="text-center pt-6 pb-4">
          <div className="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-secondary text-primary text-xs font-bold mb-5 border border-primary/20">
            <span className="w-1.5 h-1.5 rounded-full bg-primary animate-pulse" />
            مدعوم بمتوسطات السوق الحقيقية لـ MENA 2024-2025
          </div>
          <h1 className="text-3xl sm:text-5xl font-bold leading-[1.15] mb-4">
            توقعات احترافية <br className="sm:hidden" />
            <span className="text-gradient">لحملاتك الإعلانية</span>
          </h1>
          <p className="text-muted-foreground text-base sm:text-lg max-w-xl mx-auto leading-relaxed">
            أداة لفريق المبيعات تُحوّل المكالمة من تخمينات إلى تحليل مبني على بيانات صناعية ونطاقات واقعية لكل نشاط على حدة.
          </p>
        </section>

        <InputForm
          value={input}
          onChange={setInput}
          onCalculate={onCalculate}
          clientName={clientName}
          setClientName={setClientName}
        />

        <div ref={resultsRef}>
          {result && (
            <ResultsView input={input} result={result} clientName={clientName} onExport={onExport} />
          )}
        </div>

        <footer className="text-center text-xs text-muted-foreground py-8 border-t border-border/40">
          الأرقام تقديرية ومرجعية فقط — النتائج الفعلية تعتمد على جودة المحتوى والاستهداف والتحسين المستمر.
        </footer>
      </main>
    </div>
  );
};

export default Index;
