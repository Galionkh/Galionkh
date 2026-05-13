import React, { useState, useEffect } from 'react';
import { 
  BarChart, Bar, XAxis, YAxis, CartesianGrid, Tooltip, Legend, ResponsiveContainer,
  PieChart, Pie, Cell, LineChart, Line
} from 'recharts';
import { 
  Droplets, TrendingUp, TrendingDown, DollarSign, AlertCircle, 
  Activity, PieChart as PieChartIcon, ArrowDownRight, ArrowUpRight,
  LayoutDashboard, FileText, BarChart3, ListTree, Banknote
} from 'lucide-react';

// --- Helper Functions ---
const formatCurrency = (value) => {
  if (value === null || value === undefined) return '-';
  const isNegative = value < 0;
  const absValue = Math.abs(value);
  const formatted = new Intl.NumberFormat('he-IL', { maximumFractionDigits: 0 }).format(absValue);
  return isNegative ? `(${formatted})` : formatted;
};

// --- Data Extracts from PDF ---

const financialTrends = [
  { year: '2024', revenues: 141.9, costs: 95.5, netLoss: -24.9 },
  { year: '2025', revenues: 147.2, costs: 104.4, netLoss: -12.1 }
];

const expenses2025 = [
  { name: 'עלות שירותים', value: 104.4 },
  { name: 'גביה וחובות מסופקים', value: 66.4 },
  { name: 'הנהלה וכלליות', value: 7.3 }
];

const operationalMetrics = [
  { year: '2021', waterLoss: 17.49, collection: 43 },
  { year: '2022', waterLoss: 15.74, collection: 44 },
  { year: '2023', waterLoss: 16.49, collection: 46 },
  { year: '2024', waterLoss: 13.9, collection: 42 },
  { year: '2025', waterLoss: 15.6, collection: 38 }
];

const COLORS = ['#0284c7', '#f43f5e', '#64748b', '#10b981'];

// --- Full Financial Statements Data ---

const balanceSheetAssets = [
  { note: '3', name: 'מזומנים ושווי מזומנים', y2025: 6311293, y2024: 16742826 },
  { note: '4', name: 'רשויות מקומיות', y2025: 40744441, y2024: 34390877 },
  { note: '5', name: 'צרכנים', y2025: 83893299, y2024: 113201843 },
  { note: '6', name: 'חייבים שונים והוצאות מראש', y2025: 4866978, y2024: 13411297 },
  { note: '7', name: 'מלאי', y2025: 25072, y2024: 15174 },
  { note: '', name: 'סה"כ רכוש שוטף', y2025: 135841083, y2024: 177762017, isTotal: true },
  { note: '8', name: 'רכוש קבוע', y2025: 643918220, y2024: 625699547 },
  { note: '9', name: 'רכוש קבוע בהקמה בניכוי מענקים', y2025: 45706565, y2024: 12334271 },
  { note: '10', name: 'זכויות מים נטו', y2025: 2509562, y2024: 3136952 },
  { note: '11', name: 'הוצאות נדחות', y2025: 2944, y2024: 2944 },
  { note: '', name: 'סה"כ רכוש', y2025: 827978374, y2024: 818935731, isTotal: true, isGrandTotal: true },
];

const balanceSheetLiabilities = [
  { note: '12', name: 'חלויות שוטפות בגין הלוואות', y2025: 19268600, y2024: 20574433 },
  { note: '', name: 'פקיד שומה', y2025: 0, y2024: 2042896 },
  { note: '13', name: 'הוצאות לשלם', y2025: 3463407, y2024: 8690866 },
  { note: '14', name: 'ספקים ונותני שירותים', y2025: 63929267, y2024: 72404753 },
  { note: '15', name: 'עובדים ומוסדות בשל שכר', y2025: 706733, y2024: 725126 },
  { note: '16', name: 'זכאים שונים', y2025: 97913, y2024: 91870 },
  { note: '', name: 'סה"כ התחייבויות שוטפות', y2025: 87465920, y2024: 104529944, isTotal: true },
  { note: '17', name: 'הלוואות לזמן ארוך - בנקים', y2025: 58444293, y2024: 55454571 },
  { note: '18', name: 'הלוואות לזמן ארוך - רשויות', y2025: 1760146, y2024: 3809366 },
  { note: '19', name: 'הכנסות נדחות לז"א', y2025: 418230354, y2024: 383421188 },
  { note: '20', name: 'התחיבויות סיום יחסי עובד מעביד', y2025: 2399366, y2024: 1952078 },
  { note: '', name: 'סה"כ התחייבויות לזמן ארוך', y2025: 480834159, y2024: 444637203, isTotal: true },
  { note: '21', name: 'הון מניות', y2025: 172505954, y2024: 172505954 },
  { note: '', name: 'יתרת רווח (הפסד) שנצבר', y2025: 85129445, y2024: 97262630 },
  { note: '', name: 'סה"כ הון עצמי', y2025: 257635399, y2024: 269768584, isTotal: true },
  { note: '', name: 'סה"כ התחייבויות והון עצמי', y2025: 827978374, y2024: 818935731, isTotal: true, isGrandTotal: true },
];

const incomeStatementData = [
  { note: '22', name: 'הכנסות משירותי מים וביוב', y2025: 147271032, y2024: 141987325 },
  { note: '23', name: 'עלות השירותים', y2025: -104490549, y2024: -95525815 },
  { note: '', name: 'רווח (הפסד) גולמי', y2025: 42780483, y2024: 46461510, isTotal: true },
  { note: '24', name: 'עלויות גביה וחובות מסופקים', y2025: -66486109, y2024: -72520602 },
  { note: '25', name: 'הוצאות הנהלה וכלליות', y2025: -7390551, y2024: -6393756 },
  { note: '', name: 'הפסד מהפעלה', y2025: -31096177, y2024: -32452848, isTotal: true },
  { note: '26', name: 'הוצאות מימון נטו', y2025: -615317, y2024: -746188 },
  { note: '', name: 'הפסד נקי לאחר הוצ\' מימון', y2025: -31711494, y2024: -33199036, isTotal: true },
  { note: '27', name: 'הכנסות אחרות, נטו', y2025: 19578309, y2024: 8265701 },
  { note: '', name: 'הפסד נקי לפני מסים', y2025: -12133185, y2024: -24933335, isTotal: true, isGrandTotal: true },
];

const cashFlowData = [
  { note: '', name: 'הפסד לפי דוח על הרווח הכולל', y2025: -12133185, y2024: -24933335 },
  { note: 'א', name: 'התאמות (פחת, חומ"ס, שינוי ברכוש והתחייבויות)', y2025: 48164744, y2024: 55787301 },
  { note: '', name: 'מזומנים נטו שנבעו מפעילות שוטפת', y2025: 36031559, y2024: 30853966, isTotal: true },
  { note: '', name: 'השקעה בפיתוח תשתיות מים וביוב (כולל מכון טיהור)', y2025: -33372294, y2024: -23582773 },
  { note: '', name: 'השקעות בתשתיות קיימות - מים וביוב', y2025: -47194259, y2024: -42781988 },
  { note: '', name: 'מענקים והכנסות מהיטלים', y2025: 34809166, y2024: 31428309 },
  { note: '', name: 'מזומנים נטו ששימשו לפעילות השקעה', y2025: -46097761, y2024: -42878506, isTotal: true },
  { note: '', name: 'תזרימי מזומנים מפעילות מימון (פירעון הלוואות)', y2025: -365331, y2024: -6574474, isTotal: true },
  { note: '', name: 'ירידה במזומנים ושווי מזומנים', y2025: -10431533, y2024: -18599014, isTotal: true, isGrandTotal: true },
  { note: '', name: 'יתרת מזומנים לסוף השנה', y2025: 6311293, y2024: 16742826, isTotal: true, isGrandTotal: true },
];

const detailedNotesData = {
  authorities: [
    { name: 'עיריית אום אלפחם', y2025: 10306823, y2024: 7832560 },
    { name: 'עיריית טייבה', y2025: 3060511, y2024: 1577909 },
    { name: 'עיריית בקה', y2025: 10545716, y2024: 8769742 },
    { name: 'מ.מ. כפר-קרע', y2025: 6038956, y2024: 5639471 },
    { name: 'מ.מ. ערערה', y2025: 7538128, y2024: 5297559 },
    { name: 'מ.מ. מעלה עירון', y2025: 771143, y2024: 3107850 },
    { name: 'בסמ"ה', y2025: 1825016, y2024: 1746566 },
    { name: 'מ.מ. ג\'ת', y2025: 185932, y2024: 208159 },
    { name: 'מ.מ. זמר', y2025: 472216, y2024: 211061 },
    { name: 'סה"כ', y2025: 40744441, y2024: 34390877, isTotal: true }
  ],
  revenues: [
    { name: 'הכנסות ממכירת מים', y2025: 127354314, y2024: 124356326 },
    { name: 'הכנסות מהיטלי מים וזכאים', y2025: 4877841, y2024: 4304075 },
    { name: 'סה"כ הכנסות מים', y2025: 132232155, y2024: 128660401, isTotal: true },
    { name: 'הכנסות מאגרות והיטלי ביוב', y2025: 6535182, y2024: 6054940, isTotal: true },
    { name: 'הכנסות מהפעלת מט"ש ושירותים', y2025: 8503695, y2024: 7271984, isTotal: true },
    { name: 'סה"כ הכנסות', y2025: 147271032, y2024: 141987325, isGrandTotal: true }
  ],
  costs: [
    { name: 'קבלני משנה, אחזקה וחומרים (מים)', y2025: 7432493, y2024: 6186164 },
    { name: 'שכר עובדים מושאלים - מים', y2025: 11346037, y2024: 9828739 },
    { name: 'פחת תשתיות וזכויות', y2025: 632390, y2024: 646195 },
    { name: 'עלות הפקה ורכישה (מקורות וכו\')', y2025: 24127394, y2024: 22003749 },
    { name: 'עלויות איסוף והולכת שפכים', y2025: 26192029, y2024: 24916471 },
    { name: 'עלויות טיהור שפכים', y2025: 33222434, y2024: 30234474 },
    { name: 'סה"כ עלות השירותים', y2025: 104490549, y2024: 95525815, isTotal: true }
  ],
  collection: [
    { name: 'הפרשה לחובות מסופקים ואבודים', y2025: 56205000, y2024: 63765000 },
    { name: 'עמלות והוצאות גביה', y2025: 10617610, y2024: 8279730 },
    { name: 'הוצאות שכר, מיכון משרדיות וכו\'', y2025: 1309567, y2024: 1691060 },
    { name: 'בניכוי - הכנסות אכיפה', y2025: -1646068, y2024: -1215188 },
    { name: 'סה"כ', y2025: 66486109, y2024: 72520602, isTotal: true }
  ]
};

// --- Components ---

const Card = ({ children, className = '', delay = 0, isLoaded }) => (
  <div 
    className={`bg-white rounded-2xl shadow-sm border border-slate-200 overflow-hidden transition-all duration-500 ease-out transform ${isLoaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'} ${className}`}
    style={{ transitionDelay: `${delay}ms` }}
  >
    {children}
  </div>
);

const KPICard = ({ title, value, subtext, icon: Icon, trend, trendValue, delay, isLoaded }) => (
  <Card delay={delay} isLoaded={isLoaded} className="p-6 flex flex-col justify-between group hover:shadow-md transition-shadow">
    <div className="flex justify-between items-start">
      <div>
        <p className="text-slate-500 text-sm font-medium mb-1">{title}</p>
        <h3 className="text-3xl font-bold text-slate-800">{value}</h3>
      </div>
      <div className="p-3 bg-blue-50 text-blue-600 rounded-xl">
        <Icon size={24} />
      </div>
    </div>
    <div className="mt-4 flex items-center justify-between">
      <p className="text-sm text-slate-400">{subtext}</p>
      {trend && (
        <div className={`flex items-center text-sm font-semibold ${trend === 'up' ? 'text-emerald-500' : trend === 'down' ? 'text-rose-500' : 'text-slate-500'}`}>
          {trend === 'up' ? <ArrowUpRight size={16} className="ml-1" /> : <ArrowDownRight size={16} className="ml-1" />}
          <span dir="ltr">{trendValue}</span>
        </div>
      )}
    </div>
  </Card>
);

const DataTable = ({ title, data, columns, icon: Icon }) => (
  <div className="bg-white rounded-2xl shadow-sm border border-slate-200 overflow-hidden mb-8">
    <div className="bg-slate-50 border-b border-slate-200 px-6 py-4 flex items-center space-x-3 space-x-reverse">
      {Icon && <Icon size={20} className="text-blue-600" />}
      <h3 className="text-lg font-bold text-slate-800">{title}</h3>
    </div>
    <div className="overflow-x-auto">
      <table className="w-full text-right text-sm">
        <thead className="bg-slate-50 text-slate-500 border-b border-slate-200">
          <tr>
            {columns.map((col, idx) => (
              <th key={idx} className={`px-6 py-3 font-semibold ${col.align === 'center' ? 'text-center' : col.align === 'left' ? 'text-left' : 'text-right'}`}>
                {col.label}
              </th>
            ))}
          </tr>
        </thead>
        <tbody className="divide-y divide-slate-100">
          {data.map((row, idx) => (
            <tr key={idx} className={`hover:bg-slate-50 transition-colors ${row.isGrandTotal ? 'bg-slate-100 font-bold border-t-2 border-slate-300' : row.isTotal ? 'bg-slate-50 font-semibold text-blue-800' : ''}`}>
              {columns.map((col, colIdx) => (
                <td key={colIdx} className={`px-6 py-3 whitespace-nowrap ${col.align === 'center' ? 'text-center' : col.align === 'left' ? 'text-left' : 'text-right'}`}>
                  {col.format ? col.format(row[col.key]) : row[col.key]}
                </td>
              ))}
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  </div>
);

// --- Main App Component ---

export default function App() {
  const [isLoaded, setIsLoaded] = useState(false);
  const [activeTab, setActiveTab] = useState('dashboard');

  useEffect(() => {
    setTimeout(() => setIsLoaded(true), 100);
  }, []);

  const statementColumns = [
    { key: 'name', label: 'סעיף', align: 'right' },
    { key: 'note', label: 'ביאור', align: 'center' },
    { key: 'y2025', label: '2025 (₪)', align: 'left', format: formatCurrency },
    { key: 'y2024', label: '2024 (₪)', align: 'left', format: formatCurrency },
  ];

  const noteColumns = [
    { key: 'name', label: 'פירוט', align: 'right' },
    { key: 'y2025', label: '2025 (₪)', align: 'left', format: formatCurrency },
    { key: 'y2024', label: '2024 (₪)', align: 'left', format: formatCurrency },
  ];

  return (
    <div className="min-h-screen bg-slate-50 text-slate-800 font-sans pb-12" dir="rtl">
      
      {/* Header & Navigation */}
      <header className={`bg-white border-b border-slate-200 sticky top-0 z-50 transition-all duration-700 ${isLoaded ? 'opacity-100 translate-y-0' : 'opacity-0 -translate-y-4'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="py-4 flex justify-between items-center border-b border-slate-100">
            <div className="flex items-center space-x-3 space-x-reverse">
              <div className="w-12 h-12 bg-blue-600 rounded-xl flex items-center justify-center text-white shadow-md">
                <Droplets size={28} />
              </div>
              <div>
                <h1 className="text-2xl font-black text-slate-900 tracking-tight">מי עירון בע"מ</h1>
                <p className="text-sm text-slate-500 font-medium">דוח כספי מורחב - שנת 2025</p>
              </div>
            </div>
            <div className="hidden sm:flex items-center space-x-4 space-x-reverse">
              <span className="px-3 py-1 bg-emerald-100 text-emerald-700 rounded-full text-xs font-bold tracking-wide">רואה חשבון: חאלד אבו שקרה</span>
              <span className="text-sm text-slate-400">אפריל 2026</span>
            </div>
          </div>
          
          {/* Tabs Navigation */}
          <nav className="flex space-x-6 space-x-reverse overflow-x-auto py-2 hide-scrollbar">
            {[
              { id: 'dashboard', label: 'תקציר מנהלים', icon: LayoutDashboard },
              { id: 'balance', label: 'מאזן (מצב כספי)', icon: Banknote },
              { id: 'income', label: 'דוח רווח והפסד', icon: BarChart3 },
              { id: 'cashflow', label: 'תזרים מזומנים', icon: Activity },
              { id: 'notes', label: 'ביאורים ופירוטים', icon: ListTree },
            ].map((tab) => (
              <button
                key={tab.id}
                onClick={() => setActiveTab(tab.id)}
                className={`flex items-center space-x-2 space-x-reverse py-3 px-1 border-b-2 font-medium text-sm whitespace-nowrap transition-colors ${
                  activeTab === tab.id 
                    ? 'border-blue-600 text-blue-600' 
                    : 'border-transparent text-slate-500 hover:text-slate-800 hover:border-slate-300'
                }`}
              >
                <tab.icon size={18} />
                <span>{tab.label}</span>
              </button>
            ))}
          </nav>
        </div>
      </header>

      <main className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
        
        {/* --- TAB 1: DASHBOARD --- */}
        {activeTab === 'dashboard' && (
          <div className="space-y-8 animate-in fade-in duration-500">
            {/* Banner */}
            <div className={`bg-gradient-to-r from-blue-700 to-blue-500 rounded-2xl p-8 text-white shadow-lg`}>
              <h2 className="text-2xl md:text-3xl font-bold mb-3">תקציר מנהלים - שנת 2025</h2>
              <p className="text-blue-100 text-lg max-w-3xl leading-relaxed">
                שנת 2025 מתאפיינת בגידול בהכנסות וצמצום משמעותי של ההפסד הנקי (ירידה של למעלה מ-50% בהפסד). 
                עם זאת, התאגיד ממשיך להתמודד עם אתגרים תפעוליים משמעותיים: ירידה באחוזי הגבייה ל-38%, עלייה בחובות המסופקים ל-290.8 מיליון ₪ מצטבר, ועלייה בפחת המים.
              </p>
            </div>

            {/* KPIs */}
            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
              <KPICard title="סך הכנסות (2025)" value="₪147.2M" subtext="לעומת 141.9M ב-2024" icon={DollarSign} trend="up" trendValue="+3.7%" isLoaded={isLoaded} delay={100} />
              <KPICard title="הפסד נקי" value="₪(12.1M)" subtext="לעומת 24.9M- ב-2024" icon={TrendingUp} trend="up" trendValue="-51.3%" isLoaded={isLoaded} delay={200} />
              <KPICard title="פחת מים" value="15.6%" subtext="לעומת 13.9% אשתקד" icon={AlertCircle} trend="down" trendValue="+1.7%" isLoaded={isLoaded} delay={300} />
              <KPICard title="שיעור גביה שוטף" value="38%" subtext="ירידה לעומת 42% אשתקד" icon={Activity} trend="down" trendValue="-4.0%" isLoaded={isLoaded} delay={400} />
            </div>

            {/* Charts */}
            <div className="grid grid-cols-1 lg:grid-cols-2 gap-6">
              <Card isLoaded={isLoaded} delay={500} className="p-6">
                <h3 className="text-lg font-bold text-slate-800 mb-6">הכנסות מול הוצאות והפסד (במיליוני ₪)</h3>
                <div className="h-72 w-full" dir="ltr">
                  <ResponsiveContainer width="100%" height="100%">
                    <BarChart data={financialTrends} margin={{ top: 20, right: 30, left: 20, bottom: 5 }}>
                      <CartesianGrid strokeDasharray="3 3" vertical={false} stroke="#e2e8f0" />
                      <XAxis dataKey="year" axisLine={false} tickLine={false} />
                      <YAxis axisLine={false} tickLine={false} />
                      <Tooltip cursor={{fill: '#f1f5f9'}} contentStyle={{ borderRadius: '12px', border: 'none', boxShadow: '0 4px 6px -1px rgb(0 0 0 / 0.1)' }} />
                      <Legend wrapperStyle={{ paddingTop: '20px' }} />
                      <Bar dataKey="revenues" name="הכנסות" fill="#0284c7" radius={[4, 4, 0, 0]} />
                      <Bar dataKey="costs" name="עלות שירותים" fill="#64748b" radius={[4, 4, 0, 0]} />
                      <Bar dataKey="netLoss" name="הפסד נקי" fill="#f43f5e" radius={[0, 0, 4, 4]} />
                    </BarChart>
                  </ResponsiveContainer>
                </div>
              </Card>

              <Card isLoaded={isLoaded} delay={600} className="p-6">
                <h3 className="text-lg font-bold text-slate-800 mb-6">התפלגות הוצאות מרכזיות 2025</h3>
                <div className="h-72 w-full relative" dir="ltr">
                  <ResponsiveContainer width="100%" height="100%">
                    <PieChart>
                      <Pie data={expenses2025} cx="50%" cy="50%" innerRadius={60} outerRadius={100} paddingAngle={5} dataKey="value">
                        {expenses2025.map((entry, index) => <Cell key={`cell-${index}`} fill={COLORS[index % COLORS.length]} />)}
                      </Pie>
                      <Tooltip contentStyle={{ borderRadius: '12px', border: 'none', boxShadow: '0 4px 6px -1px rgb(0 0 0 / 0.1)' }} formatter={(value) => [`₪${value}M`, '']} />
                      <Legend verticalAlign="bottom" height={36} />
                    </PieChart>
                  </ResponsiveContainer>
                  <div className="absolute inset-0 flex flex-col items-center justify-center pointer-events-none pb-8">
                    <span className="text-3xl font-bold text-slate-800">₪178M</span>
                    <span className="text-xs text-slate-500">סה"כ הוצאות</span>
                  </div>
                </div>
              </Card>
            </div>
          </div>
        )}

        {/* --- TAB 2: BALANCE SHEET --- */}
        {activeTab === 'balance' && (
          <div className="space-y-6 animate-in fade-in duration-500">
            <h2 className="text-2xl font-bold text-slate-800 mb-4">דוחות על המצב הכספי (מאזן) ליום 31 בדצמבר</h2>
            <DataTable title="רכוש (נכסים)" data={balanceSheetAssets} columns={statementColumns} icon={FileText} />
            <DataTable title="התחייבויות והון עצמי" data={balanceSheetLiabilities} columns={statementColumns} icon={FileText} />
          </div>
        )}

        {/* --- TAB 3: INCOME STATEMENT --- */}
        {activeTab === 'income' && (
          <div className="space-y-6 animate-in fade-in duration-500">
            <h2 className="text-2xl font-bold text-slate-800 mb-4">דוחות על הרווח הכולל (דוח רווח והפסד)</h2>
            <DataTable title="רווח והפסד לשנה שהסתיימה ב-31 בדצמבר" data={incomeStatementData} columns={statementColumns} icon={BarChart3} />
          </div>
        )}

        {/* --- TAB 4: CASH FLOW --- */}
        {activeTab === 'cashflow' && (
          <div className="space-y-6 animate-in fade-in duration-500">
            <h2 className="text-2xl font-bold text-slate-800 mb-4">דוחות על תזרימי המזומנים</h2>
            <DataTable title="תזרים מזומנים לשנה שהסתיימה ב-31 בדצמבר" data={cashFlowData} columns={statementColumns} icon={Activity} />
          </div>
        )}

        {/* --- TAB 5: NOTES --- */}
        {activeTab === 'notes' && (
          <div className="space-y-6 animate-in fade-in duration-500">
            <h2 className="text-2xl font-bold text-slate-800 mb-4">ביאורים ופירוטים נבחרים</h2>
            <div className="grid grid-cols-1 lg:grid-cols-2 gap-8">
              <div>
                <DataTable title="ביאור 22: הכנסות משירותי מים וביוב" data={detailedNotesData.revenues} columns={noteColumns} icon={ListTree} />
                <DataTable title="ביאור 4: יתרות רשויות מקומיות" data={detailedNotesData.authorities} columns={noteColumns} icon={ListTree} />
              </div>
              <div>
                <DataTable title="ביאור 23: פירוט עלות השירותים" data={detailedNotesData.costs} columns={noteColumns} icon={ListTree} />
                <DataTable title="ביאור 24: עלויות גביה וחובות מסופקים" data={detailedNotesData.collection} columns={noteColumns} icon={ListTree} />
              </div>
            </div>
            
            {/* Context Box */}
            <div className="bg-blue-50 border border-blue-200 rounded-2xl p-6 mt-4">
              <h4 className="font-bold text-blue-800 mb-2 flex items-center">
                <AlertCircle size={20} className="mr-2" /> 
                הערות משפטיות ומיסים (ביאורים 28-30)
              </h4>
              <ul className="list-disc list-inside text-blue-900 space-y-2 text-sm">
                <li>כנגד התאגיד עומדות ותלויות 51 תביעות בסכום כולל של כ-13.2 מיליון ש"ח. הוחלט להעמיד הפרשה לתביעות תלויות בסך של כ-2 מיליון ש"ח.</li>
                <li>התאגיד חתום על 68 שעבודים (מתוכם 66 לטובת בנק מרכנתיל דיסקונט).</li>
                <li>לחברה שומות סגורות במס הכנסה עד וכולל 2020. נקבע פטור ממס חברות לשנים 2025-2026.</li>
              </ul>
            </div>
          </div>
        )}

      </main>
    </div>
  );
}
