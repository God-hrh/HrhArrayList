public class HrhArrayList {
	//默认数组大小，支持扩容，一次扩容10
	int n = 1;
	//声明一个数组做底层存储
	int[] array = new int[3];
	//数组存储元素的个数
	int size = 0;
	public static void main(String[] args) {
		HrhArrayList arrayList = new HrhArrayList();
		arrayList.add(0);
		arrayList.add(0);
		arrayList.add(0);
		arrayList.add(0,5);
		arrayList.set(1, 2);
		arrayList.delete(3);
		arrayList.print();
	}
	public HrhArrayList() {
	}
	//打印数组
	public void print() {
		for (int i = 0; i <this.size; i++) {
			System.out.print(this.array[i]+",");
		}
	}
	//末尾加入
	public void add(int element) {
		//相当于调用传入this.size
		this.add(this.size, element);
	}
	//指定位置加入
	public void add(int index,int element) {
		//对插入位置检验
		if (index < 0 || index > this.size) {
		      return;
		    }
		//支持扩容
		if (this.size>=this.array.length) {
			this.n++;
			int[] array = new int[10*this.n];
			//拷贝原数组至新扩容数组
			System.arraycopy(this.array, 0, array, 0, this.array.length);
			this.array = array;
		}
		//元素后移一位
		for (int i = this.size-1; i >= index; i--) {
			array[i+1] = array[i];
		}
		//插入该元素
		array[index] = element;
		this.size++;
	}
	public void delete(int index) {
		//对删除位置检验
		if (index < 0 || index > this.size) {
		      return;
		    }
		if (index == this.size-1) {
			this.array[this.size-1] = 0;
		}else {
			for (int i = index; i < this.size-1; i++) {
				array[index] = array[index+1];
			}
		}
		this.size--;
	}
	public void set(int index,int element) {
		//对修改位置检验
		if (index < 0 || index > this.size) {
		      return;
		    }
		this.array[index] = element;
	}
	public int size() {
		return this.size;
	}
	public int get(int index) {
		return this.array[index];
	}
}
